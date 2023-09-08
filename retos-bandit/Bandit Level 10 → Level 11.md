## Bandit Level 10→ Level 11

## Objetivo

The password for the next level is stored in the file **data.txt**, which contains base64 encoded data.
## Datos de acceso al nivel

```
Usuario: bandit10
Contraseña: G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
```
## Solución
```
Bash
bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIElGdWt3S0dzRlc4TU9xM0lSRnFyeEUxaHhUTkViVVBSCg==
bandit10@bandit:~$
bandit10@bandit:~$ echo "hola mundo"
hola mundo
bandit10@bandit:~$ echo "hola mundo" | base64
aG9sYSBtdW5kbwo=
bandit10@bandit:~$ echo -n aG9sYSBtdW5kbwo= | base64 -d
hola mundo
bandit10@bandit:~$ base64 -d data.txt
The password is IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
bandit10@bandit:~$
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIDZ6UGV6aUxkUjJSS05kTllGTmI2blZDS3pwaGxYSEJNCg==
bandit10@bandit:~$ cat data.txt | base64 -d
The password is 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
```
## Notas adicionales

| Comando | Descripción |
|-----------|-----------|
| ls | lista los archivos|
| "palo arriba"| combina varios comando en uno solo|
| cat | muestra el contenido de un archivo de texto|
| echo | se encarga de escribir un string dado en salida estandar|
| -echo -n | No imprime la nueva línea|
| base64 | codifica cadenas de caracteres|
| -base64 -d| descodifica una cadena de caracteres codificada|
## Referencias

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd
- [Base64 on Wikipedia](https://en.wikipedia.org/wiki/Base64)