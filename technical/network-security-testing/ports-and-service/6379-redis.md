# 6379 - Redis

## Identification

### Version

```
 nmap <target> -p6379 -sV
```

## Redis-cli

### Connect to host

```
redis-cli -h 10.129.254.69
```

### Show information

```
<target>:6379> info
```

### Show all keys database

```
<target>:6379> keys *
```

