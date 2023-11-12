### Safe Opener 2
## Objetivo

What can you do with this file?I forgot the key to my safe but this [file](https://artifacts.picoctf.net/c/287/SafeOpener.class) is supposed to help me with retrieving the lost key. Can you help me unlock my safe?
## Solución
```bash
alexistadeo2201-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/287/SafeOpener.class
--2023-11-12 01:27:07--  https://artifacts.picoctf.net/c/287/SafeOpener.class
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.128, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2036 (2.0K) [application/octet-stream]
Saving to: 'SafeOpener.class'

SafeOpener.class                                   100%[==============================================================================================================>]   1.99K  --.-KB/s    in 0s      

2023-11-12 01:27:07 (944 MB/s) - 'SafeOpener.class' saved [2036/2036]

alexistadeo2201-picoctf@webshell:~$ strings SafeOpener.class | grep "picoCTF"
,picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_b427942b}
alexistadeo2201-picoctf@webshell:~$ 
```
## Notas adicionales

## Bandera

picoCTF{SAf3_0p3n3rr_y0u_solv3d_it_b427942b}
## Hints

- Download and try to decompile the file.

### Referencia