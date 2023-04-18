## Cypher Anxiety Write-Up

### First Look:

After opening the challenge, we find the description as follows:

> An image was leaked from a babies store. the manager is so annoyed because he needs to identify the image to fire charges against the responsible employee. the key is the md5 of the image.
 
We see that we are given a zip file. After we download that file and extract its content, we find that there is a file in it called "find the image.pcap".

### Strings Command:

The `strings` command is a Linux command that prints the strings of printable characters in files. It is mainly useful for determining the contents of non-text files .The basic usage is fairly easy - just pass the file name as input and execute the command.

We can use the strings command to get the printable content of the pcap file that we downloaded as follows:

> strings find\ the\ image.pcap -n 10 | head -n 10

And this is the content that we got as an output:

>Sup supp, are we ready
  yeah, u got the files?
  yes but i think the channel is not secured
  the UTM will block the file transfer as the DLP module is active
  ok we can use cryptcat
  ok what the password then
  let it be P@ssawordaya
  listen on 7070 and ill send you the file , bye

We can conclude that this is some sort odf conversation between two parties and we have managed to view it. From what we have here we can conclude some points that might be useful for us to find the flag:

1. What does " the UTM will block the file transfer as the DLP module is active" mean ?
	UTM stands for Unified Threat Management. It refers to when multiple security features or services are combined into a single device within your network. DLP stands for Data Loss Prevention. It is a strategy used by organizations to ensure that sensitive data is not lost, misused, or accessed by unauthorized users. If the DLP module is active on a UTM device, it means that the UTM device is configured to monitor and prevent the transfer of sensitive data. In this case, it seems that the UTM device has detected a potential data loss incident and has blocked the file transfer as a result.
	
2. What is Cryptcat ?
	Cryptcat is a simple Unix utility which reads and writes data across network connections, using TCP or UDP protocol while encrypting the data being transmitted. It is designed to be a reliable “back-end” tool that can be used directly or easily driven by other programs and scripts. It is a standard NetCat enhanced tool with two-way encryption.
	
3. Does Cryptcat take a password ?
	Yes, Cryptcat takes a password as a salt to encrypt the data being sent over the connection. Without a specified password, Cryptcat will default to the hardcoded password “metallica”. Needless to say, failure to specify a different password makes the connection as good as unencrypted.
	
4. What is a salt in encryption ?
	In cryptography, a salt is random data that is used as an additional input to a one-way function that hashes data, a password or passphrase. Salts are used to safeguard passwords in storage. A new salt is randomly generated for each password. Typically, the salt and the password are concatenated and fed to a cryptographic hash function, and the output hash value (but not the original password) is stored with the salt in a database.
	
5. So that salt ie. password is  "P@ssawordaya".
6. The last piece of information that we got is that the port that the connection was held on was "7070".
7. What is NetCat ?
	Netcat (or nc) is a command-line utility that reads and writes data across network connections, using the TCP or UDP protocols. It is one of the most powerful tools in the network and system administrators’ arsenal and is considered as a Swiss army knife of networking tools. Netcat is cross-platform and is available for Linux, macOS, Windows, and BSD. You can use Netcat to debug and monitor network connections, scan for open ports, transfer data, as a proxy, and more.

### Using Wireshark:

After knowing the port, we can filter the packets in the pcap file by this port using "tcp.port == 7070".We get a few packets as a result of this filtering, we choose one of them then follow tcp stream. After that we change the format of the tcp stream to be "raw" and save this stream in a file.

### What's Next ? :

Now we want simulate the same scenario that happened between both parties.
Since we know that :

> Data + Key ===> Encrypted Data 

Then we can reverse this process as follows:

> Encrypted Data + Key = Data

Now we can split the terminal into two; the first is for sending the message using cryptcat and the second is for listening on port 7070 using netcat. We can do that using the following commands:

> cryptcat -l -k P@ssawordaya -p 7070 > decrypted

> netcat localhost 7070 < raw_stream 

Now if we check the decrypted file that we have made and check its type we see the following:

>decrypted: JPEG image data, JFIF standard 1.02, resolution (DPI), density 72x72, segment length 16, Exif Standard: TIFF image data, big-endian, direntries=7, orientation=upper-left, xresolution=98, yresolution=106, resolutionunit=2, software=Adobe Photoshop 7.0, datetime=2012:07:30 17:31:00, baseline, precision 8, 1600x1200, components 3

Then according to the challenge description the flag is the MD5 of the image.

Thus, using the following command:

> md5sum decrypted

We are able to find the flag.