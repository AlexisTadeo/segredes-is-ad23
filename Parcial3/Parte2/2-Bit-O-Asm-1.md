### Bit-O-Asm-1
## Objetivo

Can you figure out what is in the `eax` register? Put your answer in the picoCTF flag format: `picoCTF{n}` where `n` is the contents of the `eax` register in the decimal number base. If the answer was `0x11` your flag would be `picoCTF{17}`.Download the assembly dump [here](https://artifacts.picoctf.net/c/509/disassembler-dump0_a.txt).
## Solución
```bash
alexistadeo2201-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/509/disassembler-dump0_a.txt
--2023-11-14 19:58:09--  https://artifacts.picoctf.net/c/509/disassembler-dump0_a.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 99.84.208.73, 99.84.208.31, 99.84.208.7, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|99.84.208.73|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 209 [application/octet-stream]
Saving to: 'disassembler-dump0_a.txt'

disassembler-dump0_a.txt                           100%[==============================================================================================================>]     209  --.-KB/s    in 0s      

2023-11-14 19:58:09 (78.4 MB/s) - 'disassembler-dump0_a.txt' saved [209/209]

alexistadeo2201-picoctf@webshell:~$ cat disassembler-dump0_a.txt | grep "eax"
<+15>:    mov    eax,0x30
alexistadeo2201-picoctf@webshell:~$ python3
Python 3.10.6 (main, Aug 10 2022, 11:40:04) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print(int("0x30",16))
48
>>> exit()
alexistadeo2201-picoctf@webshell:~$ 
```
## Notas adicionales

## Bandera

picoCTF{48}
## Hints

- As with most assembly, there is a lot of noise in the instruction dump. Find the one line that pertains to this question and don't second guess yourself!
### Referencia