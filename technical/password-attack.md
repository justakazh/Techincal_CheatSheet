# Password Attack

## John The Ripper

Cracking password from /etc/shadow

```
cat /etc/passwd > passwd.txt
cat /etc/shadow > shadow.txt
unshadow shadow.txt passwd.txt > crack.txt
john --wordlist=<wordlist> crack.txt
```
