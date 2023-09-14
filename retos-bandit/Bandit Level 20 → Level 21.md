## Bandit Level 20→ Level 21

## Objetivo

There is a setuid binary in the homedirectory that does the following: it makes a connection to localhost on the port you specify as a commandline argument. It then reads a line of text from the connection and compares it to the password in the previous level (bandit20). If the password is correct, it will transmit the password for the next level (bandit21).

**NOTE:** Try connecting to your own network daemon to see if it works as you think
## Datos de acceso al nivel

```
Usuario: bandit20
Contraseña: VxCazJaVykI6W36BkBU0mJTCM8rR95XT
```
## Solución
```
Bash
bandit20@bandit:~$ nc -lnvp 2020 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT &
[1] 3444802
bandit20@bandit:~$ Listening on 0.0.0.0 2020
bandit20@bandit:~$ ./suconnect 2020
Connection received on 127.0.0.1 48964
Read: VxCazJaVykI6W36BkBU0mJTCM8rR95XT
Password matches, sending next password
NvEJF7oVjkddltPSrdKEFOllh9V1IBcq
[1]+ Done nc -lnvp 2020 <<< VxCazJaVykI6W36BkBU0mJTCM8rR95XT
bandit20@bandit:~$ exit
```
## Notas adicionales

| Comando | Descripción |
|-----------|-----------|
| nc | permite acceder a puertos TCP o UDP de la propia máquina o de otras máquinas remotas|
| -nc -l | sirve para que Netcat abra un puerto y se mantenga ala escucha|
| -nc -v | se usa para mostrar información acerca de la conexión|
| -nc -p | esta opción permite especificar el puerto al que conectarse|
| Listening | el puerto está abierto escuchando en espera de una conexión|
## Referencias

ssh, nc, cat, bash, screen, tmux, Unix ‘job control’ (bg, fg, jobs, &, CTRL-Z, …)