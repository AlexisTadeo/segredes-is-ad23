## Bandit Level 4→ Level 5

## Objetivo

The password for the next level is stored in the only human-readable file in the **inhere** directory. Tip: if your terminal is messed up, try the “reset” command.
## Datos de acceso al nivel

```
Usuario: bandit4
Contraseña: 2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
```
## Solución
```
Bash
bandit4@bandit:~$ ls
inhere
bandit4@bandit:~$ cd inhere/
bandit4@bandit:~/inhere$ ls
-file00 -file02 -file04 -file06 -file08
-file01 -file03 -file05 -file07 -file09
bandit4@bandit:~/inhere$ cat ./-file00
T
B
#6
Kt
3
6X
t
)bandit4@bandit:~/inhere$

bandit4@bandit:~/inhere$ file ./-file00
./-file00: data
bandit4@bandit:~/inhere$ file ./*
./-file00: data
./-file01: data
./-file02: data
./-file03: data
./-file04: data
./-file05: data
./-file06: data
./-file07: ASCII text
./-file08: data
./-file09: data
bandit4@bandit:~/inhere$ cat ./-file07
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
```
## Notas adicionales

| Comando | Descripción |
|-----------|-----------|
| cd | me lleva al directorio raiz|
| - cd/ | me lleva al directorio nombrado|
| cat| me muestra el contenido de un archivo|
|- cat ./|muestra el contenido de un archivo con caracteres especiales|
| ls | lista los archivos|
| file | muestra el tipo de contenido que contiene un archivo|
| - file ./ | muestra el tipo de contenido que contiene un archivo en especifico|
| - file ./* | muestra el tipo de contenido que contiene todos los archivos del directorio actual|

## Referencias

[ls](https://man7.org/linux/man-pages/man1/ls.1.html) , [cd](https://man7.org/linux/man-pages/man1/cd.1p.html) , [cat](https://man7.org/linux/man-pages/man1/cat.1.html) , [file](https://man7.org/linux/man-pages/man1/file.1.html) , [du](https://man7.org/linux/man-pages/man1/du.1.html) , [find](https://man7.org/linux/man-pages/man1/find.1.html)
