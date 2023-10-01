### strings it
## Objetivo

Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings) without running it?
## Solución
```bash
alexistadeo2201-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings
--2023-10-01 21:47:01--  https://jupiter.challenges.picoctf.org/static/fae9ac5267cd6e44124e559b901df177/strings
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 776032 (758K) [application/octet-stream]
Saving to: 'strings'

strings                                            100%[==============================================================================================================>] 757.84K  1.86MB/s    in 0.4s    

2023-10-01 21:47:01 (1.86 MB/s) - 'strings' saved [776032/776032]

alexistadeo2201-picoctf@webshell:~$ ls -la
total 836
drwxr-xr-x 4 alexistadeo2201-picoctf alexistadeo2201-picoctf   4096 Oct  1 21:47 .
drwxr-xr-x 3 root                    root                        37 Sep 25 16:29 ..
-rw-r--r-- 1 alexistadeo2201-picoctf alexistadeo2201-picoctf    220 Sep 25 16:29 .bash_logout
-rw-r--r-- 1 alexistadeo2201-picoctf alexistadeo2201-picoctf   3771 Sep 25 16:29 .bashrc
drwxrwxr-x 3 alexistadeo2201-picoctf alexistadeo2201-picoctf     19 Oct  1 21:36 .local
-rw-r--r-- 1 alexistadeo2201-picoctf alexistadeo2201-picoctf    807 Sep 25 16:29 .profile
drwx------ 2 alexistadeo2201-picoctf alexistadeo2201-picoctf     48 Sep 25 17:33 .ssh
-rw-rw-r-- 1 alexistadeo2201-picoctf alexistadeo2201-picoctf    215 Oct  1 21:47 .wget-hsts
-rw-r--r-- 1 root                    root                      4443 Oct  1 21:10 README.txt
-rw-rw-r-- 1 alexistadeo2201-picoctf alexistadeo2201-picoctf   1278 Mar 16  2023 code.py
-rw-rw-r-- 1 alexistadeo2201-picoctf alexistadeo2201-picoctf     27 Mar 16  2023 codebook.txt
-rw-rw-r-- 1 alexistadeo2201-picoctf alexistadeo2201-picoctf   1189 Mar 16  2023 convertme.py
-rw-rw-r-- 1 alexistadeo2201-picoctf alexistadeo2201-picoctf  14551 Oct 26  2020 file
-rw-rw-r-- 1 alexistadeo2201-picoctf alexistadeo2201-picoctf  14551 Oct 26  2020 file.1
-rw-rw-r-- 1 alexistadeo2201-picoctf alexistadeo2201-picoctf    705 Oct  1 21:44 fixme1.py
-rw-rw-r-- 1 alexistadeo2201-picoctf alexistadeo2201-picoctf 776032 Oct 26  2020 strings
alexistadeo2201-picoctf@webshell:~$ chmod 777 strings 
alexistadeo2201-picoctf@webshell:~$ ./strings
Maybe try the 'strings' function? Take a look at the man page
alexistadeo2201-picoctf@webshell:~$ strings strings | grep pico
picoCTF{5tRIng5_1T_7f766a23}
alexistadeo2201-picoctf@webshell:~$ 
```
## Notas adicionales

| Comando | Descripción |
## Hints

- [strings](https://linux.die.net/man/1/strings)

## Referencias