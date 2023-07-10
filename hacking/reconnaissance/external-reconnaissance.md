# External Reconnaissance

## Assets Discoveries

Mengetahui informasi asset yang dimiliki oleh target merupakan hal yang cukup penting, yang dimana kita dapat memperluas scope dan meningkatkan tingkat keberhasilan untuk masuk kedalam sebuah sistem.&#x20;

Beberapa benfit yang didapatkan dari kegiatan ini adalah :&#x20;

1. Mengetahui primary asset atau krusial oleh target
2. Mengetahui informasi main company dari target
3. Mengetaui IP Range yang terdapat pada setiap asset

### Identify Target Company / Organization

Hal pertama yang dapat kita lakukan adalah dengan melakukan information gathering terhadap identitas target perusahaan atau organisasi, kita dapat menggunakan public resource dibawah ini&#x20;

* [https://www.crunchbase.com/](https://www.crunchbase.com/)
* [https://www.linkedin.com/search/results/companies/?keywords=\<target>](https://www.linkedin.com/search/results/companies/?keywords=%3Ctarget%3E)
* [https://glints.com](https://glints.com)
* [https://www.signalhire.com](https://www.signalhire.com)
* [https://www.apollo.io/](https://www.apollo.io/)
* [https://companieshouse.id/](https://companieshouse.id/)

resource tersebut menyimpan banyak informasi perusahaan atau organisasi, sehingga memudahkan kita dalam melakukan tahap ini.

### Autonomus System Number (ASN)

ASN merupakan sebuah identifikasi numerik yang digunakan untuk mengidentifikasi jaringan otonom dalam jaringan komputer yang menggunakan protokol BGP (Border Gateway Protocol).&#x20;

Setiap jaringan otonom di internet diberikan ASN yang unik untuk mengidentifikasinya. ASN digunakan dalam pertukaran informasi routing antara jaringan-jaringan otonom. Dengan menggunakan ASN, router dan perangkat jaringan dapat mengarahkan lalu lintas secara efisien antara jaringan yang terhubung.

untuk menemukan nomor ASN target kita dapat menggunakan public resource berikut ini&#x20;

* [https://bgp.he.net](https://bgp.he.net)
* [https://asnlookup.com/](https://asnlookup.com/)

cara lain untuk mendapatkan informasi ASN target dengan menggunakan tools berikut ini

#### [amass](https://github.com/owasp-amass/amass)

```
amass intel -org "tesla"
```

