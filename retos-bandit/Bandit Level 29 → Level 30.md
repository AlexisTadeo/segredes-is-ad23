Bandit Level 29→ Level 30

## Objetivo

There is a git repository at `ssh://bandit29-git@localhost/home/bandit29-git/repo` via the port `2220`. The password for the user `bandit29-git` is the same as for the user `bandit29`.

Clone the repository and find the password for the next level.
## Datos de acceso al nivel

```
Usuario: bandit29
Contraseña: tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S
```
## Solución
```
Bash
bandit29@bandit:~$ mktemp -d

/tmp/tmp.Ir77acJZaj

bandit29@bandit:~$ cd /tmp/tmp.Ir77acJZaj

bandit29@bandit:/tmp/tmp.Ir77acJZaj$ git clone ssh://bandit29-git@localhost:2220/home/bandit29-git/repo

Cloning into 'repo'...

The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.

ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.

This key is not known by any other names

Are you sure you want to continue connecting (yes/no/[fingerprint])? yes

Could not create directory '/home/bandit29/.ssh' (Permission denied).

Failed to add the host to the list of known hosts (/home/bandit29/.ssh/known_hosts).

                         _                     _ _ _   

                        | |__   __ _ _ __   __| (_) |_ 

                        | '_ \ / _` | '_ \ / _` | | __|

                        | |_) | (_| | | | | (_| | | |_ 

                        |_.__/ \__,_|_| |_|\__,_|_|\__|

  

                      This is an OverTheWire game server. 

            More information on http://www.overthewire.org/wargames

  

bandit29-git@localhost's password: 

remote: Enumerating objects: 16, done.

remote: Counting objects: 100% (16/16), done.

remote: Compressing objects: 100% (11/11), done.

remote: Total 16 (delta 2), reused 0 (delta 0), pack-reused 0

Receiving objects: 100% (16/16), done.

Resolving deltas: 100% (2/2), done.

bandit29@bandit:/tmp/tmp.Ir77acJZaj$ ls -la

total 10564

drwx------    3 bandit29 bandit29     4096 Sep 23 04:47 .

drwxrwx-wt 4775 root     root     10801152 Sep 23 04:47 ..

drwxrwxr-x    3 bandit29 bandit29     4096 Sep 23 04:47 repo

bandit29@bandit:/tmp/tmp.Ir77acJZaj$ cd repo/

bandit29@bandit:/tmp/tmp.Ir77acJZaj/repo$ ls -la

total 16

drwxrwxr-x 3 bandit29 bandit29 4096 Sep 23 04:47 .

drwx------ 3 bandit29 bandit29 4096 Sep 23 04:47 ..

drwxrwxr-x 8 bandit29 bandit29 4096 Sep 23 04:47 .git

-rw-rw-r-- 1 bandit29 bandit29  131 Sep 23 04:47 README.md

bandit29@bandit:/tmp/tmp.Ir77acJZaj/repo$ cat README.md 

# Bandit Notes

Some notes for bandit30 of bandit.

  

## credentials

  

- username: bandit30

- password: <no passwords in production!>

  

bandit29@bandit:/tmp/tmp.Ir77acJZaj/repo$ git log --oneline

4bd5389 (HEAD -> master, origin/master, origin/HEAD) fix username

1a57cf1 initial commit of README.md

bandit29@bandit:/tmp/tmp.Ir77acJZaj/repo$ git branch -r -v

  origin/HEAD        -> origin/master

  origin/dev         13e7356 add data needed for development

  origin/master      4bd5389 fix username

  origin/sploits-dev fae3e43 add some silly exploit, just for shit and giggles

bandit29@bandit:/tmp/tmp.Ir77acJZaj/repo$ git status

On branch master

Your branch is up to date with 'origin/master'.

  

nothing to commit, working tree clean

bandit29@bandit:/tmp/tmp.Ir77acJZaj/repo$ git checkout dev

Branch 'dev' set up to track remote branch 'dev' from 'origin'.

Switched to a new branch 'dev'

bandit29@bandit:/tmp/tmp.Ir77acJZaj/repo$ ls -la

total 20

drwxrwxr-x 4 bandit29 bandit29 4096 Sep 23 04:51 .

drwx------ 3 bandit29 bandit29 4096 Sep 23 04:47 ..

drwxrwxr-x 2 bandit29 bandit29 4096 Sep 23 04:51 code

drwxrwxr-x 8 bandit29 bandit29 4096 Sep 23 04:51 .git

-rw-rw-r-- 1 bandit29 bandit29  134 Sep 23 04:51 README.md

bandit29@bandit:/tmp/tmp.Ir77acJZaj/repo$ cat README.md 

# Bandit Notes

Some notes for bandit30 of bandit.

  

## credentials

  

- username: bandit30

- password: xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS

  

bandit29@bandit:/tmp/tmp.Ir77acJZaj/repo$
```
## Notas adicionales

| Comando | Descripción |
|-----------|-----------|
| mktemp | crea una carpeta temporal|
|- mktemp -d | crea un archivo dentro de la carpeta temporal|
| cd | cambiar a un directorio o subdirectorio|
|- cd / | cambiar a un directorio o subdirectorio concreto|
| git | es un SCV (sistema de control de versiones)|
|- git clone | crea una copia de un repositorio de Git existente|
|- git checkout | cambia a una rama o commit diferente|
|- git log | como su nombre lo indica es para ver los logs|
| ls | lista los archivos|
| cat| me muestra el contenido de un archivo|
## Referencias

git