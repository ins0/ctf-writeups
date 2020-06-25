# redpwnCTF 2020
## the-library

> 249 solves / 424 points
>
> There's not a lot of useful functions in the binary itself. I wonder where you can get some...
>
> `nc 2020.redpwnc.tf 31350`
>
> Author: NotDeGhost
>
> Files: [`the-library`] [`the-library.c`] [`libc.so.6`]

#### Tags:
- pwn
- overflow
- rop
- amd64

## Summary

Overflow allow to mess up the current `stack frame`, leaking the libc addr through rop gadgets and finally spawning a shell

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
