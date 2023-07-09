---
description: 'Reconnaissance Method : Files And Directory Discovery'
---

# Files And Directory Discovery

## Preparation

Before we starting to FIles And Directory Discovery, we need a wordlist to perform and support this action, we can use SecList in this link repository below

{% embed url="https://github.com/danielmiessler/SecLists/" %}

{% hint style="info" %}
SecLists is the security tester's companion. It's a collection of multiple types of lists used during security assessments, collected in one place. List types include usernames, passwords, URLs, sensitive data patterns, fuzzing payloads, web shells, and many more.
{% endhint %}

## Discovery

### FFUF

{% embed url="https://github.com/ffuf/ffuf" %}

#### Basic Command

```
ffuf -w wordlist.txt -u http://target.tld/FUZZ 
```

#### GET Parameter&#x20;

find hidden parameter

```
ffuf -w /path/to/paramnames.txt -u https://target/script.php?FUZZ=test_value 
```

#### POST Parameter&#x20;

Brute force password&#x20;

```
ffuf -w /path/to/postdata.txt -X POST -d "username=admin\&password=FUZZ" -u https://target/login.php
```

#### Extension

find files with custom extenstion

```
ffuf -w wordlist.txt -u http://target.tld/FUZZ -e .zip,.sql,.conf
```

### Dirb

{% embed url="https://www.kali.org/tools/dirb/" %}

#### Basic Command

dirb have a default wordlist (/usr/share/dirb/common.txt), so we can direct to start scan without set the wordlist &#x20;

```
dirb http://target.tld/
```

#### Extension

find files with custom extenstion

```
dirb http://target.tld/ -X .sql
```

### Dirsearch

{% embed url="https://github.com/maurosoria/dirsearch" %}

#### Basic Command&#x20;

```
python3 dirsearch.py -u http://target.tld 
```

## View-source

as we know the View-source showing information about source code of target. so we can analyst for the potential vulnerability, find files and directory through **href** and  **src** attribute, and we can know the structure target web

<figure><img src="../../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

## Internet Archives

Internet Archive (Wayback Machine) is a system to record web urls periodically. we can use this for find target web urls

#### Resources

```
web.archive.org
index.commoncrawl.org
www.virustotal.com
```

### Waybackurl

{% embed url="https://github.com/tomnomnom/waybackurls" %}

Command

```
waybackurls example.com 
cat domain.txt | waybackurls > wayback.txt
```

## Common Sensitive Files

### Generic

```
/manifest.xml
/travis.yml
/vim_settings.xml
/database
/prod.exs
/prod.secret.exs
/.npmrc_auth
/.dockercfg
/WebServers.xmI
/sftp.json
/.exports
/.esmtprc
/sftp-config.json
/secrets.yml
/passwd
/LocalSettings.php
/config.php
/config.inc.php
/prod.secret.exs
/configuration.php
/.sh_history
/shadow
/proftpdpasswd
/.pgpass
/idea14.key
/hub
/.bash_profile
/.env
/wp-config.php
/credentials
/id_rsa
/id_dsa
/.ovpn
/.cscfg
/.rdp
/.mdf
/.sdf
/.sqlite
/.git/HEAD
/.git/config
/.psafe3
/secret_token.rb
/carrierwave.rb
/database.yml
/.keychain
/.kwallet
/config.yaml
/settings.py
/credentials.xml

```

### SQL Files

```
/db.sql
/db.sqlite
/db_backup.sql
/dbase.sql
/dbdump.sql
/setup.sql
/sqldump.sql
/dump.sql
/mysql.sql
/sql.sql
/temp.sql
/back.sql
/backup.sql
/accounts.sql
/backups.sql
/clitents.sql
/customers.sql
/data.sql
/database.sql
/database.sqlite
/users.sql

```

