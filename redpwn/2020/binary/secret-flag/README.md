# redpwnCTF 2020
## secret-flag

> 432 solves / 348 points
>
> There's a super secret flag in printf that allows you to LEAK the data at an address??
>
> `nc 2020.redpwnc.tf 31826`
>
> Author: NotDeGhost
>
> Files: [`secret-flag`]

#### Tags:
- pwn
- format string attack
- amd64

## Summary

Format string attack which leaks the flag from the current stack frame

### File
```
ELF 64-bit LSB executable,
x86-64, version 1 (SYSV),
dynamically linked,
interpreter /lib64/ld-linux-x86-64.so.2,
for GNU/Linux 3.2.0,
BuildID[sha1]=3067a5291814bef337dafc695eee28f371370eae,
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
