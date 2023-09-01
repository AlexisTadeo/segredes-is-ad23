## Bandit Level 5→ Level 6

## Objetivo

The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:

- human-readable
- 1033 bytes in size
- not executable
## Datos de acceso al nivel

```
Usuario: bandit5
Contraseña: lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
```
## Solución
```
Bash
bandit5@bandit:~$ ls
inhere
bandit5@bandit:~$ cd inhere/
bandit5@bandit:~/inhere$ ls
maybehere00 maybehere04 maybehere08 maybehere12 maybehere16
maybehere01 maybehere05 maybehere09 maybehere13 maybehere17
maybehere02 maybehere06 maybehere10 maybehere14 maybehere18
maybehere03 maybehere07 maybehere11 maybehere15 maybehere19
bandit5@bandit:~/inhere$ find . -readable -type f -size 1033c
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
```
## Notas adicionales

| Comando | Descripción |
|-----------|-----------|
| cd | me lleva al directorio raiz|
| - cd/ | me lleva al directorio nombrado|
| cat| me muestra el contenido de un archivo|
|- cat ./|muestra el contenido de un archivo con caracteres especiales|
| ls | lista los archivos|
| find | buscar un tipo archivo|
| - find . -readable | busca los archivos que contengan datos humanamente lejibles|
| - find . -type f | busca los archivos no ejecutables|
| - find . -size 0000c | busca los archivos con un tamaño de archivo en especifico|

## Referencias

[ls](https://man7.org/linux/man-pages/man1/ls.1.html) , [cd](https://man7.org/linux/man-pages/man1/cd.1p.html) , [cat](https://man7.org/linux/man-pages/man1/cat.1.html) , [file](https://man7.org/linux/man-pages/man1/file.1.html) , [du](https://man7.org/linux/man-pages/man1/du.1.html) , [find](https://man7.org/linux/man-pages/man1/find.1.html)