## Encrypted Database Write Up

After opening the challenge link, we find a website with multiple pages and it does not have any input fields so there is no hope of injecting it unyil we find any open input field. 
After that we view page source and find the following part in the page source:

> <script src="admin/assets/app.js)"></script>

Then we open the link and find that and traverse in the directories to the admin part. There we find an admin login box with two input fields one for the username and the other for the password.

After trying to inject the input fields with SQL payloads nothing worked out , so I viewed page source and found the following part in the code:

> <input type="hidden" name="db" value="secret-database/db.json" />

This indicates that there is a hidden input field and after adding this part to the URL I found the  following:

> {"flag":"ab003765f3424bf8e2c8d1d69762d72c"}

After using the website "Hash Analyzer", we find that this is an MD5 hash 
which after cracking this hash we get the flag.


