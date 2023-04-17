## Postbase Write-Up

### First: 

We can see that our text was encoded by base64.

### Second:

So  R[corrupted]BR3tCNDUzXzYxWDdZXzRSfQ==  --> As you can see we are missing some letters after 'R' , but easily we can know the number of those missing you can see if you count the letters without the corrupted section.

  --> RBR3tCNDUzXzYxWDdZXzRSfQ==  --> They're 26 and with two '==' that means that there are  two missing letters.

Just to be 28 letters so we are missing two letters after 'R' .

#### Note that in base64 the ltters should be multible of four so when we have our encoded text isn't multiple of four ,we put at the end ot it any number 0f '=' to be multiblr of four

### Third: 
Here is a python scriot to brute force the two letters:

```Python
import base64 
encodedStr = 'BR3tCNDUzXzYxWDdZXzRSfQ==' 
Map = 'ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+/=' ;

for i in range (64) : 
      for j in range (64) :
	       r= 'R' + Map[i] + Map[j] + encodedStr
	       decoded = base64.b64decode(r) 
	       if b'FLAG' in decoded :
        	 print (decoded)

```

### Last: 

After you run the script you can now see the flag --> FLAG{B453_61X7Y_4R} 