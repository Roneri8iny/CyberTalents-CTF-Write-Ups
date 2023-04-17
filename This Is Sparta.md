#  *This is Sparta Write-Up*

To find the flag we have to get the username and password correctly.
First, we inspect the page. 

We find a piece of code that seems to be written in hexa-decimal notation :

```javascript
<script>
    var _0xae5b = ["\x76\x61\x6C\x75\x65", "\x75\x73\x65\x72", "\x67\x65\x74\x45\x6C\x65\x6D\x65\x6E\x74\x42\x79\x49\x64", "\x70\x61\x73\x73", "\x43\x79\x62\x65\x72\x2d\x54\x61\x6c\x65\x6e\x74", "\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x20\x43\x6F\x6E\x67\x72\x61\x74\x7A\x20\x0A\x0A", "\x77\x72\x6F\x6E\x67\x20\x50\x61\x73\x73\x77\x6F\x72\x64"];
    function check() {
        var _0xeb80x2 = document[_0xae5b[2]](_0xae5b[1])[_0xae5b[0]];  //user info
        var _0xeb80x3 = document[_0xae5b[2]](_0xae5b[3])[_0xae5b[0]]; //password
        if (_0xeb80x2 == _0xae5b[4] && _0xeb80x3 == _0xae5b[4]) //if user = Cyber-Talent and pass  
        { alert(_0xae5b[5]); }
        else
        { alert(_0xae5b[6]); }
    }
</script>

```

After translating these hexa-decimal values using the ASCII Table at https://www.asciitable.com/
the array of `_0xae5b`  will hold the following values:

0. Value 
1. user
2. getElementById
3. pass
4. Cyber-Talent
5. Congratz
6. wrong password

The if condition states that:
> If the user = Cyber-Talent   *and*  pass = Cyber-Talent
> Then display **"Congratz"**
> Else display  **"wrong password"**   


So, this tells us that the username and password will be ***Cyber-Talent**
