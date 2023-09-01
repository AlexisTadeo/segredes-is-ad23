## Bandit Level 9→ Level 10

## Objetivo

The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.
## Datos de acceso al nivel

```
Usuario: bandit9
Contraseña: EN632PlfYiZbn3PhVK3XOGSlNInNE00t
```
## Solución
```
Bash
bandit9@bandit:~$ ls
data.txt
bandit9@bandit:~$ file data.txt
data.txt: data
bandit9@bandit:~$ strings data.txt | grep ==
c========== the
h;========== password
========== isT
n.E========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
```
## Notas adicionales

| Comando | Descripción |
|-----------|-----------|
| string | despliega las cadenas de caracteres que sean imprimibles en un archivo|
| ls | lista los archivos|
| file | muestra el tipo de contenido que contiene un archivo|
| grep | busca patrones en un archivo|
| "palo arriba"| combina varios comando en uno solo|
## Referencias

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd