# redpwnCTF 2020
## coffer-overflow-1

> 580 solves / 282 points
>
> The coffers keep getting stronger! You'll need to use the source, Luke.
>
> `nc 2020.redpwnc.tf 31255`
>
> Author: NotDeGhost
>
> Files: [`coffer-overflow-1`] [`coffer-overflow-1.c`]

#### Tags:
- pwn
- overflow
- rop
- amd64

## Summary

Stack Overflow allows to mess up the current `stack frame` and hijacking the execution flow with various ROP gadgets to pop a shell.

### File
```
 ELF 64-bit LSB executable,
x86-64, version 1 (SYSV),
dynamically linked,
interpreter /lib64/ld-linux-x86-64.so.2,
for GNU/Linux 3.2.0,
BuildID[sha1]=6a9dc1b9cad90601091c6249ccaf96dd5354440c,
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
