## Bandit Level 2 → Level 3

## Objetivo

The password for the next level is stored in a file called **spaces in this filename** located in the home directory.

## Datos de acceso al nivel

```
Usuario: bandit2
Contraseña: rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
```
## Solución
```
Bash
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ cat spaces in this filename
cat: spaces: No such file or directory
cat: in: No such file or directory
cat: this: No such file or directory
cat: filename: No such file or directory
bandit2@bandit:~$ cat spaces\ in\ this\ filename
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
bandit2@bandit:~$ cat "spaces in this filename"
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
```
## Notas adicionales

| Comando | Descripción |
|-----------|-----------|
| cat| me muestra el contenido de un archivo|
| - cat "diagonal invertida" | muestra el contenido de un archivo con espacios|
| - cat " " | otra forma de realizar el mismo comando anterior|
| ls | lista los archivos|

## Referencias

[ls](https://man7.org/linux/man-pages/man1/ls.1.html) , [cd](https://man7.org/linux/man-pages/man1/cd.1p.html) , [cat](https://man7.org/linux/man-pages/man1/cat.1.html) , [file](https://man7.org/linux/man-pages/man1/file.1.html) , [du](https://man7.org/linux/man-pages/man1/du.1.html) , [find](https://man7.org/linux/man-pages/man1/find.1.html)
- [Google Search for “spaces in filename”](https://www.google.com/search?q=spaces+in+filename)