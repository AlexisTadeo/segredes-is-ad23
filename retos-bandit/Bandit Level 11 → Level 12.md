## Bandit Level 11→ Level 12

## Objetivo

The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions.
## Datos de acceso al nivel

```
Usuario: bandit11
Contraseña: 6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
```
## Solución
```
Bash
bandit11@bandit:~$ ls
data.txt
bandit11@bandit:~$ cat data.txt
Gur cnffjbeq vf WIAOOSFzMjXXBC0KoSKBbJ8puQm5lIEi
bandit11@bandit:~$ cat data.txt | tr [a-zA-Z] [n-za-mN-ZA-M]
The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
bandit11@bandit:~$
```
## Notas adicionales

| Comando | Descripción |
|-----------|-----------|
| ls | lista los archivos|
| "palo arriba"| combina varios comando en uno solo|
| cat | muestra el contenido de un archivo de texto|
| tr | reemplaza o un conjunto de caracteres de la Entrada estándar|
## Referencias

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd
- [Rot13 on Wikipedia](https://en.wikipedia.org/wiki/Rot13)