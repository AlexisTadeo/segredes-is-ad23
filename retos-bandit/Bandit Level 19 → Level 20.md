## Bandit Level 19→ Level 20

## Objetivo

To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary.
## Datos de acceso al nivel

```
Usuario: bandit19
Contraseña: awhqfNnAbc1naukrpqDYcF95h7HoMTrC
```
## Solución
```
Bash
bandit19@bandit:~$ ls -la
total 36
drwxr-xr-x 2 root root 4096 Sep 1 06:30 .
drwxr-xr-x 49 root root 4096 Sep 1 06:30 ..
-rwsr-x--- 1 bandit20 bandit19 14872 Sep 1 06:30 bandit20-do
-rw-r--r-- 1 root root 220 Jan 6 2022 .bash_logout
-rw-r--r-- 1 root root 3771 Jan 6 2022 .bashrc
-rw-r--r-- 1 root root 807 Jan 6 2022 .profile
bandit19@bandit:~$ ./bandit20-do cat /etc/bandit_pass/bandit20
VxCazJaVykI6W36BkBU0mJTCM8rR95XT
bandit19@bandit:~$ exit
```
## Notas adicionales

| Comando | Descripción |
|-----------|-----------|
| ls | lista los archivos|
| - ls -a | muestra todos los archivos|
| - ls -l | muestra los archivos de forma mas detallada|
| cat| me muestra el contenido de un archivo|
|- cat ./|muestra el contenido de un archivo con caracteres especiales|
## Referencias

- [setuid on Wikipedia](https://en.wikipedia.org/wiki/Setuid)