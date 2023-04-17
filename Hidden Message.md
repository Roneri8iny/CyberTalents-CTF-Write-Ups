# Cyber Talents - Hidden Message WriteUp

When we first open the challenge page we find the following descrition for it as follows:

## Challenge Description
A cyber Criminal is hiding information in the below file . capture the flag ? submit Flag in MD5 Format.

As we can see there is a hidden information in the link below the description which lead us to a photo.
When we first open the link there is no much use of it so we need to download it to use some forensics tools on it so  first open your terminal on kali
and write the following command

>terminal
 wget <link of the photo>


Now after downloading it we can use exiftool to see the information of the photo

## Exiftool
ExifTool is a free and open-source software program for reading, writing, and manipulating image, audio, video, and PDF metadata.

so we can write in the terminal the following command

>terminal
 exiftool <name of the photo>


After running this command, we will get the meta data of the photo and we can see the flag in the copyright notice section.