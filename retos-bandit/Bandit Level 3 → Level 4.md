## Bandit Level 3→ Level 4

## Objetivo

The password for the next level is stored in a hidden file in the **inhere** directory.
## Datos de acceso al nivel

```
Usuario: bandit3
Contraseña: aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
```
## Solución
```
Bash
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere/
bandit3@bandit:~/inhere$ ls
bandit3@bandit:~/inhere$ ls -la
total 12
drwxr-xr-x 2 root root 4096 Jan 11 19:19 .
drwxr-xr-x 3 root root 4096 Jan 11 19:19 ..
-rw-r----- 1 bandit4 bandit3 33 Jan 11 19:19 .hidden
bandit3@bandit:~/inhere$ cat .hidden
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe
```
## Notas adicionales

| Comando | Descripción |
|-----------|-----------|
| cd | me lleva al directorio raiz|
| - cd/ | me lleva al directorio nombrado|
| cat| me muestra el contenido de un archivo|
| - cat . | muestra el contenido de un archivo que empiece con punto|
| ls | lista los archivos|
| - ls -a | muestra todos los archivos|
| - ls -l | muestra los archivos de forma mas detallada|

## Referencias

[ls](https://man7.org/linux/man-pages/man1/ls.1.html) , [cd](https://man7.org/linux/man-pages/man1/cd.1p.html) , [cat](https://man7.org/linux/man-pages/man1/cat.1.html) , [file](https://man7.org/linux/man-pages/man1/file.1.html) , [du](https://man7.org/linux/man-pages/man1/du.1.html) , [find](https://man7.org/linux/man-pages/man1/find.1.html)