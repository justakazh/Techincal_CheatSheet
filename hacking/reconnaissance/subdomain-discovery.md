# Subdomain Discovery

## Subdomain Discovery

Subdomain adalah bagian dari domain yang berada di depan domain utama, dipisahkan oleh tanda titik, misalnya : blog.example.com. Subdomain discovery adalah proses mencari dan mengidentifikasi subdomain yang terkait dengan sebuah domain utama.

Proses subdomain discovery bertujuan untuk menemukan subdomain yang mungkin tersembunyi atau tidak diketahui, karena subdomain dapat digunakan untuk mengarahkan ke berbagai layanan, aplikasi, atau infrastruktur. Menemukan subdomain dapat memberikan informasi tambahan yang berguna dalam analisis keamanan, pemetaan infrastruktur, dan penilaian serangan.

## Google Dorking

kita bisa menggunakan google dorking untuk mendapatkan subdomain yang terindex pada search engine google&#x20;

```
site:*.example.com
```

## Brute&#x20;

## Public Resources





##

### [yusub](https://github.com/justakazh/yusub)

```
yusub target.tld > domain
```

### [Sublist3r](https://github.com/aboul3la/Sublist3r)

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
