### Bit-O-Asm-2
## Objetivo

Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`.Download the assembly dump [here](https://artifacts.picoctf.net/c/510/disassembler-dump0_b.txt).
## Solución
```bash
alexistadeo2201-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/510/disassembler-dump0_b.txt
--2023-11-14 20:01:05--  https://artifacts.picoctf.net/c/510/disassembler-dump0_b.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.43, 3.160.22.16, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 270 [application/octet-stream]
Saving to: 'disassembler-dump0_b.txt'

disassembler-dump0_b.txt                           100%[==============================================================================================================>]     270  --.-KB/s    in 0s      

2023-11-14 20:01:05 (108 MB/s) - 'disassembler-dump0_b.txt' saved [270/270]

alexistadeo2201-picoctf@webshell:~$ cat disassembler-dump0_b.txt | grep "eax"
<+22>:    mov    eax,DWORD PTR [rbp-0x4]
alexistadeo2201-picoctf@webshell:~$ cat disassembler-dump0_b.txt 
<+0>:     endbr64 
<+4>:     push   rbp
<+5>:     mov    rbp,rsp
<+8>:     mov    DWORD PTR [rbp-0x14],edi
<+11>:    mov    QWORD PTR [rbp-0x20],rsi
<+15>:    mov    DWORD PTR [rbp-0x4],0x9fe1a
<+22>:    mov    eax,DWORD PTR [rbp-0x4]
<+25>:    pop    rbp
<+26>:    ret
alexistadeo2201-picoctf@webshell:~$ python3
Python 3.10.6 (main, Aug 10 2022, 11:40:04) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print(int("0x9fe1a",16))
654874
>>> exit()
alexistadeo2201-picoctf@webshell:~$ 
```
## Notas adicionales

## Bandera

picoCTF{654874}
## Hints

- `PTR`'s or 'pointers', reference a location in memory where values can be stored.
### Referencia