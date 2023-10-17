### Glory of the Garden
## Objetivo

This [garden](https://jupiter.challenges.picoctf.org/static/4153422e18d40363e7ffc7e15a108683/garden.jpg) contains more than it seems.
## Solución
```bash
alexistadeo2201-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/4153422e18d40363e7ffc7e15a108683/garden.jpg
--2023-10-17 01:53:23--  https://jupiter.challenges.picoctf.org/static/4153422e18d40363e7ffc7e15a108683/garden.jpg
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 2295192 (2.2M) [application/octet-stream]
Saving to: 'garden.jpg'

garden.jpg                                         100%[==============================================================================================================>]   2.19M  1.82MB/s    in 1.2s    

2023-10-17 01:53:24 (1.82 MB/s) - 'garden.jpg' saved [2295192/2295192]

alexistadeo2201-picoctf@webshell:~$ strings garden.jpg | grep "picoCTF"
Here is a flag "picoCTF{more_than_m33ts_the_3y33dd2eEF5}"
alexistadeo2201-picoctf@webshell:~$ 
```
## Notas adicionales


## Bandera

picoCTF{more_than_m33ts_the_3y33dd2eEF5}
## Hints

- What is a hex editor?