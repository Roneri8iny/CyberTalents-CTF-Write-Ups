# *I am a Legend Write-Up*

After opening the challeng link, we get a page that requires a username and a password.
We have to inspect the page, after doing that we will find a piece of code that has the following characters '\]' , '\[' and '+'.
After some research , I found that this is called "JavaScript-fuck obfuscated text".

## *Obfuscation*

In software development, the term Obfuscation basically refers to the technique of making the source code of some application/program difficult to read for some other person, letting the functionality be the same as it was earlier.

### *Why Obfuscation?*

1.  **Helps in optimizing the code and provides a faster experience**
2.  **Makes reverse engineering a longer process**
3. **Prevents people from copying your code**

### *How Obfuscation?*

1.  **Garbage Code Insertion**
2. **Encoding (Custom / Pre-defined methods)**

    > atob()  --> for decoding a base64 encoded string
    > btoa()  --> for encoding a string to base64 

3. **Renaming functions and variables**
   In this case, the developers rename the functions and variables with gibberish text, hexadecimal patterns etc to make the reading and debugging process harder for someone who’s not familiar with the flow of control of the code.

After decoding that code using http://deobfuscatejavascript.com/ we got:

```javascript
String.fromCharCode(102, 117, 110, 99, 116, 105, 111, 110, 32, 99, 104, 101, 99, 107, 40, 41, 123, 10, 10, 118, 97, 114, 32, 117, 115, 101, 114, 32, 61, 32, 100, 111, 99, 117, 109, 101, 110, 116, 91, 34, 103, 101, 116, 69, 108, 101, 109, 101, 110, 116, 66, 121, 73, 100, 34, 93, 40, 34, 117, 115, 101, 114, 34, 41, 91, 34, 118, 97, 108, 117, 101, 34, 93, 59, 10, 118, 97, 114, 32, 112, 97, 115, 115, 32, 61, 32, 100, 111, 99, 117, 109, 101, 110, 116, 91, 34, 103, 101, 116, 69, 108, 101, 109, 101, 110, 116, 66, 121, 73, 100, 34, 93, 40, 34, 112, 97, 115, 115, 34, 41, 91, 34, 118, 97, 108, 117, 101, 34, 93, 59, 10, 10, 105, 102, 40, 117, 115, 101, 114, 61, 61, 34, 67, 121, 98, 101, 114, 34, 32, 38, 38, 32, 112, 97, 115, 115, 61, 61, 32, 34, 84, 97, 108, 101, 110, 116, 34, 41, 123, 97, 108, 101, 114, 116, 40, 34, 32, 32, 32, 32, 32, 32, 32, 32, 32, 32, 32, 32, 32, 32, 32, 32, 32, 32, 32, 32, 32, 32, 67, 111, 110, 103, 114, 97, 116, 122, 32, 92, 110, 32, 70, 108, 97, 103, 58, 32, 123, 74, 52, 86, 52, 95, 83, 99, 114, 49, 80, 116, 95, 49, 83, 95, 83, 48, 95, 68, 52, 77, 78, 95, 70, 85, 78, 125, 34, 41, 59, 125, 32, 10, 101, 108, 115, 101, 32, 123, 97, 108, 101, 114, 116, 40, 34, 119, 114, 111, 110, 103, 32, 80, 97, 115, 115, 119, 111, 114, 100, 34, 41, 59, 125, 125)
```

Then, going to the a new tab, we open the developer tools then we write this code in the console, to get:

```javascript

'function check(){\n\nvar user = document["getElementById"]("user")["value"];\nvar pass = document["getElementById"]("pass")["value"];\n\nif(user=="Cyber" && pass== "Talent"){alert("                      Congratz \\n Flag: {J4V4_Scr1Pt_1S_S0_D4MN_FUN}");} \nelse {alert("wrong Password");}}'

```

Thus, we see the flag, the username and password.