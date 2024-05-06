# Subdomain Discovery

## Subdomain Discovery

Subdomain adalah bagian dari domain yang berada di depan domain utama, dipisahkan oleh tanda titik, misalnya : blog.example.com. Subdomain discovery adalah proses mencari dan mengidentifikasi subdomain yang terkait dengan sebuah domain utama. subdomain discovery bertujuan untuk menemukan subdomain yang mungkin tersembunyi atau tidak diketahui, karena subdomain dapat digunakan untuk mengarahkan ke berbagai layanan, aplikasi, atau infrastruktur. dengan menemukan banyak subdomain dapat memberikan informasi tambahan yang berguna dalam analisis keamanan, pemetaan infrastruktur, dan penilaian serangan.

### Google Dorking

kita bisa menggunakan google dorking untuk mendapatkan subdomain yang terindex pada search engine google&#x20;

```
site:*.example.com
```

### Brute Force

mencoba menemukan subdomain yang ada di bawah sebuah domain target dengan mencoba berbagai kombinasi subdomain secara otomatis dan melakukan pengecheckan terhadap response status HTTP.&#x20;

#### [ffuf](https://github.com/ffuf/ffuf)

```bash
ffuf -w SecLists/Discovery/DNS/namelist.txt -u http://FUZZ.taget.tld 

#virtual host
ffuf -w SecLists/Discovery/DNS/namelist.txt -H "Host: FUZZ.site.com" -u http://taget.tld -fs {size}
```

#### [gobuster](https://github.com/OJ/gobuster)

```bash
gobuster dns -d target.tld -t 50 -w subdomains.txt
```

#### [shuffledns](https://github.com/projectdiscovery/shuffledns)

```bash
shuffledns -d target.tld -list subdomains.txt -r resolvers.txt
```

### DNS

kita dapat menemukan subdomain dengan melakukan pengecheckan terhadap DNS. kita dapat melihat DNS Record yang menyimpan informasi penting tentang konfigurasi domain, seperti alamat IP, server mail, server name server (NS), catatan MX, dan sebagainya. selain itu kita juga bisa melakukan pengecheckan terhadap **Zone Transfer**.

#### [dnsrecon](https://github.com/darkoperator/dnsrecon)

```
dnsrecon -a -d tesla.com
```

#### dig

```
dig target.tld
dig axfr target.tld @server.target.tld
```





### [yusub](https://github.com/justakazh/yusub)

```
yusub target.tld > domain
```

### [Sublist3r](https://github.com/aboul3la/Sublist3r)

```bash
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
