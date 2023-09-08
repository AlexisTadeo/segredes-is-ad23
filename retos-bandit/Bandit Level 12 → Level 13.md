## Bandit Level 12→ Level 13

## Objetivo

The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work using mkdir. For example: mkdir /tmp/myname123. Then copy the datafile using cp, and rename it using mv (read the manpages!).
## Datos de acceso al nivel

```
Usuario: bandit12
Contraseña: JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
```
## Solución
```
Bash
bandit12@bandit:~$ xxd -r data.txt | file -
/dev/stdin: gzip compressed data, was "data2.bin", last modified: Thu May 7 18:14:30 2020, max compression, from Unix
bandit12@bandit:~$
bandit12@bandit:~$
bandit12@bandit:~$ xxd -r data.txt | zcat |file -
/dev/stdin: bzip2 compressed data, block size = 900k
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat |file -
/dev/stdin: gzip compressed data, was "data4.bin", last modified: Thu May 7 18:14:30 2020, max compression, from Unix
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat |file -
/dev/stdin: POSIX tar archive (GNU)
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | file -
/dev/stdin: POSIX tar archive (GNU)
bandit12@bandit:~$
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | file -
/dev/stdin: bzip2 compressed data, block size = 900k
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat |file -
/dev/stdin: POSIX tar archive (GNU)
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | file -
/dev/stdin: gzip compressed data, was "data9.bin", last modified: Thu May 7 18:14:30 2020, max compression, from Unix
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat | file -
/dev/stdin: ASCII text
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
```
## Notas adicionales

| Comando | Descripción |
|-----------|-----------|
| xxd | tranforma una linea de caracteres a un vaciado exadecimal|
| -xxd -r | revierte el proceso del vaciado exadecimal|
| file | muestra el tipo de contenido que contiene un archivo|

Algunos tipos de compresion en Linux

| extencion | comprecion | descomprecion | ver en consola |
| --- | ------- | ----- | --------------- |
|.gz| gzip| gzip -d (gunzip)| zcat|
|.bz2 | bzip2 | bzip2 -d (bunzip2) | bzcat|
|.tar |tar |tar xf |tar xO|

otros (instalar) :

| .zip | zip | unzip (7z x)|
| ----- | --- | ----------- |
| .rar | rar | unrar (7z x)|
## Referencias

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd, mkdir, cp, mv, file
- [Hex dump on Wikipedia](https://en.wikipedia.org/wiki/Hex_dump)