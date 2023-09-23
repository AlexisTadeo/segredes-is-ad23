Bandit Level 30→ Level 31

## Objetivo

There is a git repository at `ssh://bandit30-git@localhost/home/bandit30-git/repo` via the port `2220`. The password for the user `bandit30-git` is the same as for the user `bandit30`.

Clone the repository and find the password for the next level.
## Datos de acceso al nivel

```
Usuario: bandit30
Contraseña: xbhV3HpNGlTIdnjUrdAlPzc2L6y9EOnS
```
## Solución
```
Bash
bandit30@bandit:~$ mktemp -d

/tmp/tmp.9iNfG5Mo7c

bandit30@bandit:~$ cd /tmp/tmp.9iNfG5Mo7c

bandit30@bandit:/tmp/tmp.9iNfG5Mo7c$ git clone ssh://bandit30-git@localhost:2220/home/bandit30-git/repo

Cloning into 'repo'...

The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.

ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.

This key is not known by any other names

Are you sure you want to continue connecting (yes/no/[fingerprint])? yes

Could not create directory '/home/bandit30/.ssh' (Permission denied).

Failed to add the host to the list of known hosts (/home/bandit30/.ssh/known_hosts).

                         _                     _ _ _   

                        | |__   __ _ _ __   __| (_) |_ 

                        | '_ \ / _` | '_ \ / _` | | __|

                        | |_) | (_| | | | | (_| | | |_ 

                        |_.__/ \__,_|_| |_|\__,_|_|\__|

  

                      This is an OverTheWire game server. 

            More information on http://www.overthewire.org/wargames

  

bandit30-git@localhost's password: 

remote: Enumerating objects: 4, done.

remote: Counting objects: 100% (4/4), done.

remote: Total 4 (delta 0), reused 0 (delta 0), pack-reused 0

Receiving objects: 100% (4/4), done.

bandit30@bandit:/tmp/tmp.9iNfG5Mo7c$ cd repo/

bandit30@bandit:/tmp/tmp.9iNfG5Mo7c/repo$ ls -la

total 16

drwxrwxr-x 3 bandit30 bandit30 4096 Sep 23 04:56 .

drwx------ 3 bandit30 bandit30 4096 Sep 23 04:56 ..

drwxrwxr-x 8 bandit30 bandit30 4096 Sep 23 04:56 .git

-rw-rw-r-- 1 bandit30 bandit30   30 Sep 23 04:56 README.md

bandit30@bandit:/tmp/tmp.9iNfG5Mo7c/repo$ cat README.md 

just an epmty file... muahaha

bandit30@bandit:/tmp/tmp.9iNfG5Mo7c/repo$ git log --oneline

59530d3 (HEAD -> master, origin/master, origin/HEAD) initial commit of README.md

bandit30@bandit:/tmp/tmp.9iNfG5Mo7c/repo$ git branch -rv

  origin/HEAD   -> origin/master

  origin/master 59530d3 initial commit of README.md

bandit30@bandit:/tmp/tmp.9iNfG5Mo7c/repo$ git ls-remote

The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.

ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.

This key is not known by any other names

Are you sure you want to continue connecting (yes/no/[fingerprint])? yes

Could not create directory '/home/bandit30/.ssh' (Permission denied).

Failed to add the host to the list of known hosts (/home/bandit30/.ssh/known_hosts).

                         _                     _ _ _   

                        | |__   __ _ _ __   __| (_) |_ 

                        | '_ \ / _` | '_ \ / _` | | __|

                        | |_) | (_| | | | | (_| | | |_ 

                        |_.__/ \__,_|_| |_|\__,_|_|\__|

  

                      This is an OverTheWire game server. 

            More information on http://www.overthewire.org/wargames

  

bandit30-git@localhost's password: 

From ssh://bandit30-git@localhost:2220/home/bandit30-git/repo

59530d30d299ff2e3e9719c096ebf46a65cc1424 HEAD

59530d30d299ff2e3e9719c096ebf46a65cc1424 refs/heads/master

831aac2e2341f009e40e46392a4f5dd318483019 refs/tags/secret

bandit30@bandit:/tmp/tmp.9iNfG5Mo7c/repo$ ls -la

total 16

drwxrwxr-x 3 bandit30 bandit30 4096 Sep 23 04:56 .

drwx------ 3 bandit30 bandit30 4096 Sep 23 04:56 ..

drwxrwxr-x 8 bandit30 bandit30 4096 Sep 23 04:56 .git

-rw-rw-r-- 1 bandit30 bandit30   30 Sep 23 04:56 README.md

bandit30@bandit:/tmp/tmp.9iNfG5Mo7c/repo$ git checkout refs/tags/secret 

fatal: reference is not a tree: refs/tags/secret

bandit30@bandit:/tmp/tmp.9iNfG5Mo7c/repo$ git branch -a

* master

  remotes/origin/HEAD -> origin/master

  remotes/origin/master

bandit30@bandit:/tmp/tmp.9iNfG5Mo7c/repo$ git checkout remotes/origin/master

Note: switching to 'remotes/origin/master'.

  

You are in 'detached HEAD' state. You can look around, make experimental

changes and commit them, and you can discard any commits you make in this

state without impacting any branches by switching back to a branch.

  

If you want to create a new branch to retain commits you create, you may

do so (now or later) by using -c with the switch command. Example:

  

  git switch -c <new-branch-name>

  

Or undo this operation with:

  

  git switch -

  

Turn off this advice by setting config variable advice.detachedHead to false

  

HEAD is now at 59530d3 initial commit of README.md

bandit30@bandit:/tmp/tmp.9iNfG5Mo7c/repo$ ls -la

total 16

drwxrwxr-x 3 bandit30 bandit30 4096 Sep 23 04:56 .

drwx------ 3 bandit30 bandit30 4096 Sep 23 04:56 ..

drwxrwxr-x 8 bandit30 bandit30 4096 Sep 23 05:01 .git

-rw-rw-r-- 1 bandit30 bandit30   30 Sep 23 04:56 README.md

bandit30@bandit:/tmp/tmp.9iNfG5Mo7c/repo$ git checkout HEAD

bandit30@bandit:/tmp/tmp.9iNfG5Mo7c/repo$ ls -la

total 16

drwxrwxr-x 3 bandit30 bandit30 4096 Sep 23 04:56 .

drwx------ 3 bandit30 bandit30 4096 Sep 23 04:56 ..

drwxrwxr-x 8 bandit30 bandit30 4096 Sep 23 05:02 .git

-rw-rw-r-- 1 bandit30 bandit30   30 Sep 23 04:56 README.md

bandit30@bandit:/tmp/tmp.9iNfG5Mo7c/repo$ cat README.md 

just an epmty file... muahaha

bandit30@bandit:/tmp/tmp.9iNfG5Mo7c/repo$ git remote show refs/tags/secret

fatal: 'refs/tags/secret' does not appear to be a git repository

fatal: Could not read from remote repository.

  

Please make sure you have the correct access rights

and the repository exists.

bandit30@bandit:/tmp/tmp.9iNfG5Mo7c/repo$ git ls-remote

The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.

ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.

This key is not known by any other names

Are you sure you want to continue connecting (yes/no/[fingerprint])? yes

Could not create directory '/home/bandit30/.ssh' (Permission denied).

Failed to add the host to the list of known hosts (/home/bandit30/.ssh/known_hosts).

                         _                     _ _ _   

                        | |__   __ _ _ __   __| (_) |_ 

                        | '_ \ / _` | '_ \ / _` | | __|

                        | |_) | (_| | | | | (_| | | |_ 

                        |_.__/ \__,_|_| |_|\__,_|_|\__|

  

                      This is an OverTheWire game server. 

            More information on http://www.overthewire.org/wargames

  

bandit30-git@localhost's password: 

From ssh://bandit30-git@localhost:2220/home/bandit30-git/repo

59530d30d299ff2e3e9719c096ebf46a65cc1424 HEAD

59530d30d299ff2e3e9719c096ebf46a65cc1424 refs/heads/master

831aac2e2341f009e40e46392a4f5dd318483019 refs/tags/secret

bandit30@bandit:/tmp/tmp.9iNfG5Mo7c/repo$ git cat-file -p 831aac2e2341f009e40e46392a4f5dd318483019

OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt

bandit30@bandit:/tmp/tmp.9iNfG5Mo7c/repo$
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
|- git -ls remote | permite crear, ver y eliminar conexiones con otros repositorios.|
|- git cat-file -p | Para ver el contenido de un object en el sistema de archivos de git|
| ls | lista los archivos|
| cat| me muestra el contenido de un archivo|
## Referencias

git