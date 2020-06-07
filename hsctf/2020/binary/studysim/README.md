# HSCTF 7
## StudySim

> 495
>
> We created a small program to help you keep track of your increasing workload.
>
> Connect to make use of our organizer at `nc pwn.hsctf.com 5007`.
>
> Author: PMP
>
> Files: [`libc.so.6`] [`ld-2.29.so`] [`studysim`]

#### Tags:
- pwn
- heap
- malloc
- tcache
- negative overflow
- glibc 2.29
- amd64

## Summary

Duo to not checking a negative index we are able to get a `partial write anywhere`. With the partial write we injecting fake tcache entries which allows to gain a full `read anywhere` and `write anywhere` priv. With (almost) full binary protection we then use a `one-gadget` and `malloc_hook` to gain RIP control and a shell.  

### File
```
ELF 64-bit LSB executable, x86-64, version 1 (SYSV)
dynamically linked
interpreter /mnt/share/hsctf/2020/binary/StudySim/ld-2.29.so
for GNU/Linux 3.2.0
BuildID[sha1]=5fef3a9da00afad488567bfcbdff45beb687e534
not stripped
```

### Checksec
```
Full RELRO
Canary found
NX enabled
No PIE
```
