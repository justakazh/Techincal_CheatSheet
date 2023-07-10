# Domain Discovery

## Domain Discovery

Pada tahap ini kita dapat melakukan identifikasi dan menemukan domain yang terkait dengan suatu entitas, seperti perusahaan, organisasi, atau individu.

### Google Dorking

kita bisa menemukan domain target dengan google dorking. kita dapat menggunakan informasi yang telah ditemukan sebelumnya pada tahap [assets-discovery.md](assets-discovery.md "mention").

```
intext:"targetname"
intitle:"targetname"
```

biasanya referensi yang akan diberikan akan menampilkan atau menghubungkan pada domain target tersebut.

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

#### [punter](https://github.com/nethunteros/punter)

```
python main.py -t google.com
```

