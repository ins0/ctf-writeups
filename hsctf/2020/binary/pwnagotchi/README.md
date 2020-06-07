# HSCTF 7
## Boredom

> 116
>
> Have fun with your new pwnagotchi!
>
> Connect to view your \ (•-•) / at `nc pwn.hsctf.com 5005`.
>
> Author: meow
>
> Files: [`pwnagotchi`]

#### Tags:
- pwn
- overflow
- rop
- amd64

## Summary

Basic overflow allow to mess up the current `stack frame` and hijacking the execution flow with various ROP gadgets to leak a `libc` address and jumping to a one-gadget to gain a shell.

### File
```
ELF 64-bit LSB executable, x86-64, version 1 (SYSV)
dynamically linked
interpreter /lib64/ld-linux-x86-64.so.2
for GNU/Linux 3.2.0
BuildID[sha1]=f8c34ef43ba5a8fbce8b89987797d88f7adbb31f
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
