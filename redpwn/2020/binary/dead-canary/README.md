# redpwnCTF 2020
## dead-canary

> 96 solves / 475 points
>
> It is a terrible crime to slay a canary. Killing a canary will keep your exploit alive even if you are an inch from segfaults. But at a terrible price.
>
> `nc 2020.redpwnc.tf 31744`
>
> Author: NotDeGhost
>
> Files: [`dead-canary`]

#### Tags:
- pwn
- format string attack
- rop
- canary
- amd64

## Summary

Format String attack with infinity read/write. We first override stack fail with main, leaking a stack and libc addr. After that using a rop to pop a shell.

### File
```
ELF 64-bit
LSB executable,
x86-64, version 1 (SYSV),
dynamically linked,
interpreter /lib64/ld-linux-x86-64.so.2,
for GNU/Linux 3.2.0,
BuildID[sha1]=34839e5a32490988b85d8efcbddecc1673110ecc,
stripped
```

### Checksec
```
Partial RELRO
Canary found
NX enabled
No PIE
No RPATH
No RUNPATH
No Symbols
```
