# redpwnCTF 2020
## coffer-overflow-2

> 530 solves / 304 points
>
> You'll have to jump to a function now!?
>
> `nc 2020.redpwnc.tf 31908`
>
> Author: NotDeGhost
>
> Files: [`coffer-overflow-2`] [`coffer-overflow-2.c`]

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
BuildID[sha1]=0904cdb0421222a7323625c5e603d5368a2e9928,
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
