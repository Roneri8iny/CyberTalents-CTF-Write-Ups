## Guess The Password Write-Up

### Using hash analyzer we find that its type is sha1 or sha128.

Since sha1 is weaker than sha128 we start to crack it assuming that it is sha1.

Then we start to search for a website that cracks sha1 hashes.

After searching for a while , I found this website https://md5hashing.net/hash/sha1 , and using it to crack the sha1 hash we get the flag.

> The Flag : jrahyn+


