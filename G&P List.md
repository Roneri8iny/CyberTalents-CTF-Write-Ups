## G&P List Write-Up

### First Thoughts:

After a opening the file, I found that it seems to be an ordinary word file but of course this is not the case. 

### Binwalk:

> Binwalk is a tool for searching a given binary image for embedded files and executable code .Specifically, it is designed for identifying files and code embedded inside of firmware images. Binwalk uses the libmagic library, so it is compatible with magic signatures created for the Unix file utility. We can also use it with files with the flag '-e' to extract hidden files or executable code.

After doing that we find a new directory that is named  G&P+lists.docx.extracted . Then we traverse inside this directory we find a file that is named Flag.txt. We open that file to find the flag in it.


