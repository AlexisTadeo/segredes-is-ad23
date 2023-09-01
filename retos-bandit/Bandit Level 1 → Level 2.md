## Bandit Level 1 → Level 2

## Objetivo

The password for the next level is stored in a file called **-** located in the home directory.

## Datos de acceso al nivel

```
Usuario: bandit1
Contraseña: NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL
```
## Solución
```
Bash
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat -
^C
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$ pwd
/home/bandit1
bandit1@bandit:~$ cat /home/bandit1/-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
```
## Notas adicionales

| Comando | Descripción |
|-----------|-----------|
| pwd | me indica el directorio actual|
| cat| me muestra el contenido de un archivo|
|- cat ./|muestra el contenido de un archivo con caracteres especiales|
| ls | lista los archivos|

## Referencias

[ls](https://man7.org/linux/man-pages/man1/ls.1.html) , [cd](https://man7.org/linux/man-pages/man1/cd.1p.html) , [cat](https://man7.org/linux/man-pages/man1/cat.1.html) , [file](https://man7.org/linux/man-pages/man1/file.1.html) , [du](https://man7.org/linux/man-pages/man1/du.1.html) , [find](https://man7.org/linux/man-pages/man1/find.1.html)
- [Google Search for “dashed filename”](https://www.google.com/search?q=dashed+filename)
- [Advanced Bash-scripting Guide - Chapter 3 - Special Characters](http://tldp.org/LDP/abs/html/special-chars.html)