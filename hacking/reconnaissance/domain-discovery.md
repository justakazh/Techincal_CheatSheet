# Domain Discovery

## Domain Discovery

Pada tahap ini kita dapat melakukan identifikasi dan menemukan domain yang terkait dengan suatu entitas, seperti perusahaan, organisasi, atau individu.

### Search Engine

kita dapat mengembangkan informasi yang kita dapatkan pada tahap [assets-discovery.md](assets-discovery.md "mention")  menggunakan search engine untuk mendapatkan informasi domain yang dimiliki oleh target

```
intext:"targetname"
intitle:"targetname"
```

#### Unique keyword

kita juga dapat menggunakan keyword unik yang terdapat pada target, misalnya kita bisa menggunakan copyright yang biasanya terdapat pada footer

```
intext:"copyright @ <taget>"
```

### Reverse Whois&#x20;

kita dapat melakukan reverse whois yang dimana teknik ini digunakan untuk mencari domain atau informasi domain dengan mencari berdasarkan kriteria atau atribut tertentu, seperti nama pemilik, alamat email, kata kunci, atau informasi lainnya. kita juga dapat menggunakan informasi yang didapatkan pada tahap [assets-discovery.md](assets-discovery.md "mention")

#### Public Resources

* [https://viewdns.info/reversewhois/?q=\<target>](https://viewdns.info/reversewhois/?q=%3Ctarget%3E)
* [https://domaineye.com/reverse-whois](https://domaineye.com/reverse-whois)
* [https://www.whoxy.com/](https://www.whoxy.com/)
* [https://www.reversewhois.io/](https://www.reversewhois.io/)
* [https://reversewhois.domaintools.com/](https://reversewhois.domaintools.com/)
* [https://whoisology.com/](https://whoisology.com/)
* [https://dnslytics.com/search?q=\<target>](https://dnslytics.com/search?q=%3Ctarget%3E)

#### [DomLink](https://github.com/vysecurity/DomLink)

```
python domLink.py -D target.com -o target.out.txt
```

#### [amass](https://github.com/owasp-amass/amass)

```
amass intel -d tesla.com -whois
```

ASN Reverse Whois

```
amass intel -asn 54888 -whois  -d tesla.com
```

#### [punter](https://github.com/nethunteros/punter)

```
python main.py -t google.com
```

### Reverse Google Analytics

Terkadang beberapa domain saling menggunakan owner Google Analiytic yang sama, hal ini dapat kita manfaatkan untuk menemukan domain lainnya yang dimiliki oleh target. selain itu Google Adsense juga dapat digunakan dalam kegiatan ini.

#### Public Resources

* [https://osint.sh/analytics/](https://osint.sh/analytics/)
* [https://hackertarget.com/reverse-analytics-search/](https://hackertarget.com/reverse-analytics-search/)

#### [udon](https://github.com/dhn/udon)

```
udon -silent -json -s UA-33427076 | jq -c
```

### Favicon

favicon adalah gambar kecil yang digunakan untuk mewakili sebuah situs web atau aplikasi di browser. Favicon memiliki hash unik dan dapat memberikan petunjuk atau indikasi tentang identitas dan karakteristik situs web target. &#x20;

untuk mendapatkan hash dari favicon kita dapat menggunakan script berikut ini&#x20;

```python
import requests
import mmh3

response = requests.get("http://target.tld/favicon.ico")
favicon = response.content.encode("base64")
hash = mmh3.hash(favicon)
print(hash)
```

#### Public Resources

* [https://www.shodan.io/search?query=http.favicon.hash](https://www.shodan.io/search?query=http.favicon.hash%3A116323821):[\<hash>](https://www.shodan.io/search?query=)

#### [favfreak](https://app.gitbook.com/s/aq0Im6nGlIt1tgViGqFC/page)

```
cat urls.txt | python3 favfreak.py -o output
```

#### [Shodan](https://help.shodan.io/command-line-interface/0-installation)

```
shodan search org:"Target" http.favicon.hash:116323821 --fields ip_str,port --separator " " | awk '{print $1":"$2}'
```
