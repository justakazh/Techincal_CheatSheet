---
description: >-
  Beberapa sumber atau tools online yang berguna pada saat OSINT / Recon /
  Information Gathering.
---

# Usefull  Resource

## Web Based

Beberapa sumber berguna berbasis web yang dapat digunakan untuk mendapatkan informasi dan mempercepat pekerjaan.&#x20;

### Multipurposes

sumber dibawah ini sangat berguna untuk kebutuhan pasive reconnaissance, yang dimana mereka merupakan Internet Intelligence Platform yang dapat yang menyediakan banyak data yang terekspos di internet.

* [https://censys.io/](https://censys.io/https://www.yougetsignal.com/https://app.netlas.io/https://shodan.io/https://fullhunt.io/https://www.zoomeye.org/https://leakix.net/https://www.criminalip.io/https://intelx.io/https://onyphe.io/https://pentest-tools.com/https://domaineye.com/)
* [https://www.yougetsignal.com/](https://censys.io/https://www.yougetsignal.com/https://app.netlas.io/https://shodan.io/https://fullhunt.io/https://www.zoomeye.org/https://leakix.net/https://www.criminalip.io/https://intelx.io/https://onyphe.io/https://pentest-tools.com/https://domaineye.com/)
* [https://app.netlas.io/](https://censys.io/https://www.yougetsignal.com/https://app.netlas.io/https://shodan.io/https://fullhunt.io/https://www.zoomeye.org/https://leakix.net/https://www.criminalip.io/https://intelx.io/https://onyphe.io/https://pentest-tools.com/https://domaineye.com/)
* [https://shodan.io/](https://shodan.io/)
* [https://fullhunt.io/](https://fullhunt.io/)
* [https://www.zoomeye.org/](https://www.zoomeye.org/)
* [https://leakix.net/](https://leakix.net/)
* [https://www.criminalip.io/](https://www.criminalip.io/)
* [https://intelx.io/](https://intelx.io/)
* [https://onyphe.io/](https://onyphe.io/)
* [https://pentest-tools.com/](https://pentest-tools.com/)
* [https://domaineye.com/](https://domaineye.com/)

### Identify Company/Organization Detail

Kadang kita juga perlu tahu detail sebuah company atau organisasi untuk mendapatkan informasi ekstra seperti contohnya orang ada didalam sebuah company atau organisasi tersebut. submber dibawah ini dapat digunakan untuk mendapatkan informasi tersebut

* [https://www.crunchbase.com/](https://www.crunchbase.com/)
* [https://www.linkedin.com/search/results/companies/?keywords=\<target>](https://www.linkedin.com/search/results/companies/?keywords=%3Ctarget%3E)
* [https://glints.com/](https://glints.com/)
* [https://www.signalhire.com](https://www.signalhire.com)
* [https://www.apollo.io/](https://www.apollo.io/)
* [https://companieshouse.id/](https://companieshouse.id/)

### Code Search Engine

Sumber berikut ini dapat digunakan untuk mendapatkan informasi dari sebuah source code atau syntax, jika beruntung kita bisa saja mendapatkan source code target yang terekspos

* [https://publicwww.com/](https://publicwww.com/)
* [https://github.com/](https://github.com/)
* [https://grep.app/](https://grep.app/)
* [https://searchcode.com](https://searchcode.com)

### Find E-Mail

Sumber berikut ini sangat cocok untuk volunteer vulnerability disclosure atau bug hunter dalam mencari kontak developer atau pemilik asset sebuah target

* [https://hunter.io](https://hunter.io)
* [https://thatsthem.com/reverse-email-lookup](https://thatsthem.com/reverse-email-lookup)
* [https://www.voilanorbert.com/](https://www.voilanorbert.com/)
* [http://www.skymem.info/](http://www.skymem.info/)

### Username Search Engine

sumber dibawah ini sangat cocok untuk mencari akun target pada social media atau platform lain.&#x20;

* [https://checkusernames.com/](https://checkusernames.com/)
* [https://instantusername.com/](https://instantusername.com/)

### Exif Data

Sumber dibawah ini digunakan untuk melihat atau menampilkan exif data dari sebuah file

* [https://exif-viewer.com](https://exif-viewer.com)

### Find Secret API Key

sumber ini untuk mencari Secret API KEY, sangat memudahkan dalam melakukan static analyst

* [https://serene-agnesi-57a014.netlify.app/](https://serene-agnesi-57a014.netlify.app/)

### API Search Engine

Sumber ini untuk mencari API pada target, sangat berguna untuk mendapatkan informasi endpoint dan memperluas serangan

* [https://rapidapi.com/](https://rapidapi.com/)
* [https://www.postman.com/explore/](https://www.postman.com/explore/)

### Darkweb Exposure Check

Sumber ini dapat digunakan untuk mengecheck kebocoran data pada target, tentunya kita bisa mendapatkan juicy information milik target

* [https://www.immuniweb.com/darkweb/](https://www.immuniweb.com/darkweb/)

### Tehcnology Identifier

```
https://www.wappalyzer.com/
```

## Dorks

Beberapa dork yang dapat digunakan untuk mendapatkan informasi yang terekspos pada search engine seperti google

### E-Mail Search&#x20;

Mencari alamat email target company atau organisasi

```
intext:"@target.tld" 
intitle:"contact us" intext:"@target.tld"
```

## CLI BASED

Beberapa tools berguna berbasis command line interface yang dapat digunakan untuk mendapatkan informasi dan mempercepat pekerjaan.&#x20;

### Amass

[https://github.com/owasp-amass/amass](https://github.com/owasp-amass/amass)

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

