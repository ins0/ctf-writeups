# HSCTF 7
## Got It

> 425
>
> Oh no, someone's messed with my GOT entries, and now my function calls are all wrong! Please, you have to help me! I'll do anything to make my function calls right!
>
> This is running on Ubuntu 18.04, with the standard libc.
>
> Connect with `nc pwn.hsctf.com 5004`.
>
> Author: PMP
>
> Files: [`got_it`] [`Dockerfile`]

#### Tags:
- pwn
- format attack
- got override
- amd64

## Summary

User Input is passed as format identifier and allows arbitrary read/write. Overriding `exit` with `main` to gain ∞ read/write. Leak `libc` and call `system("/bin/sh)` through swapped `scanf` with `system` 

### File
```
ELF 64-bit LSB executable, x86-64, version 1 (SYSV)
dynamically linked
interpreter /lib64/ld-linux-x86-64.so.2
BuildID[sha1]=6ea73b9292490795954e28c84bc26a05a3fc6c1f
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
