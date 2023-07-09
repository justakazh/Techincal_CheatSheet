# 21 - FTP

## Identification

### Version&#x20;

```
nmap -sV -p21 <target>
```

### Nmap Script

```
nmap -p21 --script=<script> <target>

#scan all script

nmap -p21 --script=ftp-* <target>
```

## Default Configuration

### Anonymous Login

```
ftp <target>
usename : anonymous
password : <blank>
```
