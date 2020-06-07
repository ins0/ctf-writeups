# HSCTF 7
## Boredom

> 100
>
> Keith is bored and stuck at home. Give him some things to do.
>
>Connect at `nc pwn.hsctf.com 5002`.
>
> Author: PMP
>
> Files: [`boredom.c`] [`boredom`]

#### Tags:
- pwn
- overflow
- amd64

## Summary

Basic overflow allow to mess up the current `stack frame` and overriding the `ret` address and jumping to the `flag` function 

### File
```
ELF 64-bit LSB executable, x86-64, version 1 (SYSV)
dynamically linked
interpreter /lib64/ld-linux-x86-64.so.2
BuildID[sha1]=99a762a8f8f05784a81b593573ca8252f44ecc7e
for GNU/Linux 3.2.0
not stripped
```

### Checksec
```
Full RELRO
No canary found
NX enabled
No PIE
No RPATH
No RUNPATH 
```
