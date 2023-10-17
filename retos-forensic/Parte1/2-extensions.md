### extensions
## Objetivo

This is a really weird text file [TXT](https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt)? Can you find the flag?
## Solución
```bash
alexistadeo2201-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt
--2023-10-17 01:57:17--  https://jupiter.challenges.picoctf.org/static/e7e5d188621ee705ceeb0452525412ef/flag.txt
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 9984 (9.8K) [application/octet-stream]
Saving to: 'flag.txt'

flag.txt                                           100%[==============================================================================================================>]   9.75K  --.-KB/s    in 0s      

2023-10-17 01:57:17 (181 MB/s) - 'flag.txt' saved [9984/9984]

alexistadeo2201-picoctf@webshell:~$ ls
flag.txt
alexistadeo2201-picoctf@webshell:~$ mv flag.txt flag.png 
alexistadeo2201-picoctf@webshell:~$ ls
flag.png
alexistadeo2201-picoctf@webshell:~$ 
```
## Notas adicionales

| Comando | Descripción |
|-----------|-----------|
| mv | Sirve para cambiar el formato de un archivo|
## Bandera

picoCTF{now_you_know_about_extensions}
## Hints

- How do operating systems know what kind of file it is? (It's not just the ending!
- Make sure to submit the flag as picoCTF{XXXXX}