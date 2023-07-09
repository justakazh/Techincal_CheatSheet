# URLs

## URLS

by collecting url, u can know web structure and potential to found juicy information&#x20;

### GAU

{% embed url="https://github.com/lc/gau" %}

#### Installation

```
go install github.com/lc/gau/v2/cmd/gau@latest
```

#### Basic Command

```
cat domain.txt | gau 
```

### Waybackurl

{% embed url="https://github.com/tomnomnom/waybackurls" %}

#### Installation

```
go install github.com/tomnomnom/waybackurls@latest
```

#### Basic Command

```
cat domains.txt | waybackurls > data
cat data | grep .sql
```

### Linkfinder

{% embed url="https://github.com/GerbenJavado/LinkFinder" %}

#### Installation

```
git clone https://github.com/GerbenJavado/LinkFinder.git
cd LinkFinder
python setup.py install
```

#### Basic Command

```
python3 linkfinder.py -i https://target.tld -d
```

### Arjun

{% embed url="https://github.com/s0md3v/Arjun" %}

#### Installation

```
git clone https://github.com/s0md3v/Arjun
cd Arjun
python3 setup.py install
```

#### Basic Command

```
arjun -u https://api.example.com/endpoint
```
