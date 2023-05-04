## Newsletter Write-Up

After opening the challenge link, we find an input field that requires an email.
At first I tried some scripts to see if there is an XSS vulnerability but nothing seemed to work out and no matter what I entered it required that the entered characters must contain '@' and '.' for the email to be valid.

After that I tried using Burp Suite and entered the email "test@test.com" in order to be a valid email so that the request can pass on to be intercepted by Burp Suite.

After intercepting the request, I sent the packet to the repeater in order to modify the request to try and find the flag.

If we look at the description of the challeng, we find that it says the following;

> the administrator put the backup file in the same root folder as the application, help us download this backup by retrieving the backup file name

That means that we can pass the request with the format of an email and then pipe it on to any command that could help us find the backup file.

We can modify the request as follows:

> email=test@.|pwd|| 

This will give us a reply with the current working directory and that is :

> /var/www/html/newsletter

Then we can pass on the request as follows:

>  email=test@.|ls|| 

That gives us all the files and directories present in the directory we are currently in, which are:

> emails.txt
> hgdr64.ackup.tar.gz
> index.php

Thus we can see the name of the backup file and that means that we have found the flag.