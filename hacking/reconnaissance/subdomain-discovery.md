---
description: 'Reconnaissance Method : Subdomain Discovery'
---

# Subdomain Discovery

## D

### Yusub

### Basic Command

```
yusub target.tld > domain
```

### Sublist3r

{% embed url="https://github.com/aboul3la/Sublist3r" %}

#### Installation

```
git clone https://github.com/aboul3la/Sublist3r
sudo pip install -r requirements.txt
```

#### Basic Command

```
python sublist3r.py -d example.com
```

## Active

### FFUF

#### Subdomain Brute Force

```
ffuf -w /opt/SecLists/Discovery/DNS/subdomains-top1million-110000.txt -u http://trick.htb -H "Host: preprod-FUZZ.trick.htb" -fs 5480
```

### Dig

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption><p><a href="https://www.youtube.com/watch?v=rQ-dc5kwRtU">https://www.youtube.com/watch?v=rQ-dc5kwRtU</a></p></figcaption></figure>

#### DNS Zone transfer check

```
dig axfr trick.htb @trick.htb
```

enumerate the DNS servers to confirm the system’s name

```
dig @<ip> +short <domain> any
```
