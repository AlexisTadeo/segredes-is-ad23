## Bandit Level 8→ Level 9

## Objetivo

The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once
## Datos de acceso al nivel

```
Usuario: bandit8
Contraseña: TESKZC0XvTetK0S9xNwm25STk5iWrBvP
```
## Solución
```
Bash
bandit8@bandit:~$ ls
data.txt
bandit8@bandit:~$ wc data.txt
1001 1001 33033 data.txt
bandit8@bandit:~$ cat data.txt | sort | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
```
## Notas adicionales

| Comando | Descripción |
|-----------|-----------|
| cat| me muestra el contenido de un archivo|
| ls | lista los archivos|
| wc | muestra la cantidad de lineas, datos y bytes que contiene un archivo|
| sort | ordena las lineas de forma alfabetica dentro de un archivo|
| "palo arriba"| combina varios comando en uno solo|
| uniq | muestra tipos de busqueda de lineas en un archivo|
| -uniq -u | muestra las linea en un archivo que son unicos (que no se repiten)|
## Referencias

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd
- [Piping and Redirection](https://ryanstutorials.net/linuxtutorial/piping.php)