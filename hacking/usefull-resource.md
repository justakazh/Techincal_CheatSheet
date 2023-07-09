---
description: >-
  Beberapa sumber atau tools online yang berguna pada saat OSINT / Recon /
  Information Gathering.
---

# Usefull Resource

## Public Resources

### Multipurposes

```
https://censys.io/
https://www.yougetsignal.com/
https://app.netlas.io/
https://shodan.io/
https://fullhunt.io/
https://www.zoomeye.org/
https://leakix.net/
https://www.criminalip.io/
https://intelx.io/
https://onyphe.io/
https://pentest-tools.com/
https://domaineye.com/
```

### Identify Company/Organization Detail

```
https://www.crunchbase.com/
https://www.linkedin.com/search/results/companies/?keywords=<target>
https://glints.com/
https://www.signalhire.com
https://www.apollo.io/
https://companieshouse.id/
```

### Code Search Engine

```
https://publicwww.com/
https://grep.app/
https://github.com/
https://searchcode.com
```

### Find E-Mail

```
https://hunter.io
https://thatsthem.com/reverse-email-lookup
https://www.voilanorbert.com/
http://www.skymem.info/
```

### Username Search Engine

```
https://checkusernames.com/
https://instantusername.com/
```

### Exif Data

```
https://exif-viewer.com
```

### Find Secret API Key

```
https://serene-agnesi-57a014.netlify.app/
```

### API Search Engine

```
https://rapidapi.com/
https://www.postman.com/explore/
```

### Darkweb Exposure Check

```
https://www.immuniweb.com/darkweb/
```

### Tehcnology Profiler

```
https://www.wappalyzer.com/
```

## Dorks

### E-Mail Search&#x20;

```
intext:"@target.tld" 
intitle:"contact us" intext:"@target.tld"
```

## Amass

{% embed url="https://github.com/OWASP/Amass" %}

### Find ASN

```
amass intel -org "<organization>"
amass intel -org "Tesla"
```

### Reverse Whois

```
amass intel -active -asn <asn number> -whois -d <domain>
amass intel -active -asn 1337 -whois -d target.tld
```
