---
description: Identify operating system target used
---

# OS Fingerprinting

## Identification

to identify operating system we can see the TTL (Time To Live) Response&#x20;

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption><p><a href="https://www.semanticscholar.org/paper/Packet-Inspection-for-Unauthorized-OS-Detection-in-Tyagi-Paul/880095d7fe063c9553a3f958c050996682e5ec9e/figure/1">https://www.semanticscholar.org/paper/Packet-Inspection-for-Unauthorized-OS-Detection-in-Tyagi-Paul/880095d7fe063c9553a3f958c050996682e5ec9e/figure/1</a></p></figcaption></figure>

### Ping

<div align="left">

<figure><img src="../../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

</div>

**Basic Command**

```
ping 1.1.1.1
```

### Nmap

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

**Basic Command**

```
nmap -O 1.1.1.1
```

### Response HTTP Header

### Error Message

### PHPINFO

### ASP / ASPX

