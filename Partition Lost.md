# Cyber Talents - Partition Lost Write up 

When we first open the challenge  page , the description tells us that 
the CEO of a company had a car accident and his HDD was damaged and he lost 
all his files and partitiions and they want us to recover imporatnt data from the patition 

So first let's download the partition image file from the link provided in the challenge 

Then open the terminal in kali  and write the following command

```Terminal
strings partition-lost.img | grep -oiP "flag(.*)" 
```

> The command reads the contents of the partition file and uses the strings command to extract 
 printable strings from the file and then pipes the output of the strings to grep command to search for a string 
 that matches the regular expression "flag(.*)". The -o option specifies that only the matching string should be printed, and the -i option specifies 
 that the search should be case-insensitive.

It gave us a long list of flags so let's try to filter it a little by adding the `-n` flag to the 
strings command.

```Terminal
strings -n 8 partition-lost.img | grep -oiP "flag(.*)"
```

It also gave us a long list of flags so let's add the tail command to find the final flag

```Terminal
strings -n 8 partition-lost.img | grep -oiP "flag(.*)" | tail -n 1 
```

After that you will find the flag.



