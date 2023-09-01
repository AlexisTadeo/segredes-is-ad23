## Bandit Level 7→ Level 8

## Objetivo

The password for the next level is stored in the file **data.txt** next to the word **millionth**
## Datos de acceso al nivel

```
Usuario: bandit7
Contraseña: z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
```
## Solución
```
Bash
bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ wc data.txt
98567 197133 4184396 data.txt
bandit7@bandit:~$ grep millionth data.txt
millionth TESKZC0XvTetK0S9xNwm25STk5iWrBvP
bandit7@bandit:~$ cat data.txt | grep millionth
millionth TESKZC0XvTetK0S9xNwm25STk5iWrBvP
```
## Notas adicionales

| Comando | Descripción |
|-----------|-----------|
| cat| me muestra el contenido de un archivo|
| ls | lista los archivos|
| wc | muestra la cantidad de lineas, datos y bytes que contiene un archivo|
| grep | busca patrones en un archivo|
| "palo arriba"| combina varios comando en uno solo|
## Referencias

[man](https://man7.org/linux/man-pages/man1/man.1.html), grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd