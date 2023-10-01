### Static ain't always noise
## Objetivo
Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/static)? This [BASH script](https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/ltdis.sh) might help!
## Solución
```bash
alexistadeo2201-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/static
alexistadeo2201-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/66932732825076cad4ba43e463dae82f/ltdis.sh
alexistadeo2201-picoctf@webshell:~$ ls -la
total 52
drwxr-xr-x 2 alexistadeo2201-picoctf alexistadeo2201-picoctf   131 Sep 25 17:08 .
drwxr-xr-x 3 root                    root                       37 Sep 25 16:29 ..
-rw-r--r-- 1 alexistadeo2201-picoctf alexistadeo2201-picoctf   220 Sep 25 16:29 .bash_logout
-rw-r--r-- 1 alexistadeo2201-picoctf alexistadeo2201-picoctf  3771 Sep 25 16:29 .bashrc
-rw-r--r-- 1 alexistadeo2201-picoctf alexistadeo2201-picoctf   807 Sep 25 16:29 .profile
-rw-rw-r-- 1 alexistadeo2201-picoctf alexistadeo2201-picoctf   167 Sep 25 16:35 .wget-hsts
-rw-r--r-- 1 root                    root                     4443 Sep 25 17:07 README.txt
-rw-rw-r-- 1 alexistadeo2201-picoctf alexistadeo2201-picoctf    34 Mar 16  2021 flag
-rw-rw-r-- 1 alexistadeo2201-picoctf alexistadeo2201-picoctf  8376 Mar 16  2021 static
-rw-rw-r-- 1 alexistadeo2201-picoctf alexistadeo2201-picoctf 10936 Mar 16  2021 warm
alexistadeo2201-picoctf@webshell:~$ file static
static: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=277d07901cf99a335a8107fbdd6642d9c6140bb5, not stripped
alexistadeo2201-picoctf@webshell:~$ chmod +x static
alexistadeo2201-picoctf@webshell:~$ ./static
Oh hai! Wait what? A flag? Yes, it's around here somewhere!
alexistadeo2201-picoctf@webshell:~$ strings static | grep pico
picoCTF{d15a5m_t34s3r_f5aeda17}
alexistadeo2201-picoctf@webshell:~$ 
```
## Notas adicionales

| Comando | Descripción |
|-----------|-----------|
## Hints