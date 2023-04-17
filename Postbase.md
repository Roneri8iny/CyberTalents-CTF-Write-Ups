### Challenge Description:

> We got this letters and numbers and don't understand them. Can you? R[corrupted]BR3tCNDUzXzYxWDdZXzRSfQ==

The format of this encoding indicates that this is a base64 encoding, that is because there are two "=" signs at the end of it. We also need to know the number of characters in it to assess how many characters are missing. We can use the following website "lettercount.com" to do so. We find that it is 26 charactes that means that there are 2 missing characters to get 28 sharacters to be a multiple of 4. So, we can write a simple code that attempts to brute force the missing two characters.

```Python 
import base64  
encodedStr = 'BR3tCNDUzXzYxWDdZXzRSfQ=='  
Map = 'ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+/=' ;  
  
for i in range (64) :  
      for j in range (64) :  
           r= 'R' + Map[i] + Map[j] + encodedStr;  
           decoded = base64.b64decode(r);  
           if b'FLAG' in decoded :  
                print(decoded)
```

After running this code snippet, we get the flag in the format:

> FLAG{#############}

