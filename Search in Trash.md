# Cyber Talents - Search in Trash Writeup

When se first open the challenge, the description tells us the an HDD is damaged in an accident but it was able to recover
his recycle bin file. He wants us to find the flag in that file.

So first we will download the file on kali using the `wget` command 
Then after downloading the file we can notice that their is a text file with the same name so let's try to 
`cat` it in the terminal 

```Terminal
cat 'file name'
```

After searching through the output you can find the flag.
