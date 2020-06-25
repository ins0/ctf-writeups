# redpwnCTF 2020
## coffer-overflow-0

> 873 solves / 179 points
>
> Can you fill up the coffers? We even managed to find the source for you.
>
> `nc 2020.redpwnc.tf 31199`
>
> Author: NotDeGhost
>
> Files: [`coffer-overflow-0`] [`coffer-overflow-0.c`]

#### Tags:
- pwn
- overflow
- amd64

## Summary

Basic overflow allow to mess up the current `stack frame` and overriding a local variable that allows to spawn a shell

### File
```
ELF 64-bit LSB executable,
x86-64, version 1 (SYSV),
dynamically linked, 
interpreter /lib64/ld-linux-x86-64.so.2,
for GNU/Linux 3.2.0,
BuildID[sha1]=4ed4ec837e4bbcc455f484c105c0fb5d0ca61b2d,
not stripped
```

### Checksec
```
Partial RELRO
No canary found
NX enabled
No PIE
No RPATH
No RUNPATH
```
