# Local Enumeration

## System

### Hostname

kita perlu mengidentifikasi hostname dari sebuah sistem, alasannya ini dapat mempermudah kita untuk mengidentifikasi dimesin mana kita saat ini

```
hostname
```

### Operating system

pada dasarnya setiap sistem operasi yang digunakan berbeda-beda, baik itu dari segi versi, distro dan kernel. kita dapat mengetahui terkait sistem operasi yang digunakan secara spesifik dengan menggunakan perintah berikut ini

```
cat /etc/issue
cat /etc/*-release
cat /etc/lsb-release
cat /etc/redhat-release
cat /proc/version
uname -a
uname -mrs
rpm -q kernel
dmesg | grep Linux
```

## Users Enumeration

untuk mengetahui user yang terdaftar pada sebuah mesin kita dapat menjalankan perintah berikut ini

```
cat /etc/passwd
```

## Users Environment

Setiap penguna pada linux memiliki environmentnya sendiri, terkadang mereka menyisipkan beberapa informasi menarik pada environment

```
env
```

### Bash Configuration

mereka terkadang juga menyisipkan informasi pada beberapa configuration files&#x20;

```
cat /etc/profile
cat /etc/bashrc
cat ~/.bash_profile
cat ~/.bashrc
cat ~/.bash_logout
cat ~/.zshrc
```

### Bash History

ketika kita berhasil mendapatkan akses pada sebuah user, kita dapat melihat perintah yang telah dijalankan user tersebut dengan mengetikan perintah dibawah ini

```
history
```

cara lain untuk mengetahuinya kita dapat melihat file .bash\_history

```
cat .bash_history
```

## Network Enumeration

pada dasarnya setiap sistem memiliki IP, kita dapat mengetahuinya dengan perintah berikut ini&#x20;

```
ip a
```

selain IP yang dapat diketahui dengan perintah diatas tersebut, kita juga dapat mengetahui interface yang tersedia. dengan mengetahui informasi ip yang terdapat pada sebuah mesin, memungkinkan kita untuk memberikan gambaran terkait mesin yang dapat kita lakukan pivot.

### Route

kita dapat melihat kemana network dirouting dengan perintah berikut

```
ip route
```

### Local service enumeration

sebuah sistem biasanya menjalankan service yang tidak dapat diakses oleh publik, hal ini dapat kita ketahui dengan menggunakan perintah berikut ini&#x20;

```
netstat -aon
```

