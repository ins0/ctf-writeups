# redpwnCTF 2020
## skywriting

> 80 solves / 480 points
>
> It's pretty intuitive once you disambiguate some homoglyphs, I don't get why nobody solved it...
>
> `nc 2020.redpwnc.tf 31034`
>
> Author: NotDeGhost
>
> Files: [`skywriting`]

#### Tags:
- pwn
- overflow
- canary
- amd64

## Summary

Overflow which allows to leak the canary and a libc addr and also prepare a rop after the main functions leaves, which pops a shell.

### File
```
ELF 64-bit LSB shared object,
x86-64, version 1 (SYSV),
dynamically linked,
interpreter /lib64/ld-linux-x86-64.so.2,
for GNU/Linux 3.2.0,
BuildID[sha1]=a9593754c5c05d17f9cfdbccb170a49e323b33eb,
stripped
```

### Checksec
```
Full RELRO
Canary found
NX enabled
PIE enabled
No RPATH
No RUNPATH
No Symbols
```
