# One Liner Command

## Probing using HTTPX

```
#by @beginnbounty
cat domain.txt | httpx -follow-redirects -status-code -vhost -threads 100 -silent | sort -u | grep "[200]" | cut -d [ -f1 | short -u | sed ' s/[[:blank:]]*$//' | tee prober
```
