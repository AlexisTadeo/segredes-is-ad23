## Bandit Level 6→ Level 7

## Objetivo

The password for the next level is stored **somewhere on the server** and has all of the following properties:

- owned by user bandit7
- owned by group bandit6
- 33 bytes in size
## Datos de acceso al nivel

```
Usuario: bandit6
Contraseña: P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
```
## Solución
```
Bash
bandit6@bandit:~$ ls
bandit6@bandit:~$ ls -la
total 20
drwxr-xr-x 2 root root 4096 Jan 11 19:18 .
drwxr-xr-x 70 root root 4096 Jan 11 19:19 ..
-rw-r--r-- 1 root root 220 Jan 6 2022 .bash_logout
-rw-r--r-- 1 root root 3771 Jan 6 2022 .bashrc
-rw-r--r-- 1 root root 807 Jan 6 2022 .profile
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
```
## Notas adicionales

| Comando | Descripción |
|-----------|-----------|
| cat| me muestra el contenido de un archivo|
|- cat /|muestra el contenido de un archivo que este en un directorio en especifico|
| ls | lista los archivos|
| - ls -a | muestra todos los archivos|
| - ls -l | muestra los archivos de forma mas detallada|
| find | buscar un tipo archivo|
| - find / -user | busca los archivos que este relacionados con un usuario en especifico|
| - find / -group | busca los archivos que este relacionados con un grupo en especifico|
| - find / -size 0000c | busca los archivos con un tamaño de archivo en especifico|
| - find /  2>/dev/null | manda todos los archivos buscados que tengan un error al limbo|

## Referencias

[ls](https://man7.org/linux/man-pages/man1/ls.1.html) , [cd](https://man7.org/linux/man-pages/man1/cd.1p.html) , [cat](https://man7.org/linux/man-pages/man1/cat.1.html) , [file](https://man7.org/linux/man-pages/man1/file.1.html) , [du](https://man7.org/linux/man-pages/man1/du.1.html) , [find](https://man7.org/linux/man-pages/man1/find.1.html)