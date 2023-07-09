---
description: 'Reconnaissance Method : Favicon Hashes'
---

# Favicon Hashes

### Pengantar

Favicon merupakan sebuah icon yang berfungsi untuk branding sebuah website, setiap favicon memiliki hash yang unik dan kita dapat memanfaatkan hash tersebut untuk melakukan pencarian server, domain, dan subdomain.



### FavFreak

FavFreak mendeteksi hash dari favicon dan secara otomatis melakukan information gathering dari  shodan dengan menggunakan katakunci hash tersebut

{% embed url="https://github.com/devanshbatham/FavFreak" %}

#### Installation

```
git clone https://github.com/devanshbatham/FavFreak
cd FavFreak
python3 -m pip install mmh3
cat urls.txt | python3 favfreak.py 

```

#### Basic Command

```
cat urls.txt | python3 favfreak.py -o output
```

