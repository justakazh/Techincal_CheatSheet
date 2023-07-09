---
description: Discovery alive host from target
---

# Host Discovery

## Getting IP from domain

### Nslookup

<div align="left">

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

</div>

**Basic Command**

```
nslookup example.com
```

### Ping

<div align="left">

<figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

</div>

**Basic Command**

```
ping example.com
```



## Discovery

### Nmap

{% embed url="https://nmap.org/" %}

<div align="left">

<figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

</div>

**Basic Command**

```
nmap -sn 1.1.1.0/24
```

### Fping

{% embed url="https://github.com/schweikert/fping" %}

<div align="left">

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

</div>

**Basic Command**

```
ping -a -g 1.1.1.0/24 
```

**Only show alive ip**

```
ping -a -g 1.1.1.0/24 2>/dev/null
```

### Reverse DNS (identify hostname)

```
nmap -sL 1.1.1.1
```

## Related Article&#x20;

{% embed url="https://justakazh.medium.com/1-1-reconnaissance-host-discovery-53ae1e3f104f" %}

{% embed url="https://www.techtarget.com/searchnetworking/definition/ping-sweep-ICMP-sweep" %}

{% embed url="https://nmap.org/book/man-host-discovery.html" %}
