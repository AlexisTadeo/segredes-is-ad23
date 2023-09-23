Bandit Level 28→ Level 29

## Objetivo

There is a git repository at `ssh://bandit28-git@localhost/home/bandit28-git/repo` via the port `2220`. The password for the user `bandit28-git` is the same as for the user `bandit28`.

Clone the repository and find the password for the next level.
## Datos de acceso al nivel

```
Usuario: bandit28
Contraseña: AVanL161y9rsbcJIsFHuw35rjaOM19nR
```
## Solución
```
Bash
bandit28@bandit:~$ mktemp -d

/tmp/tmp.e7BlmeyGE3

bandit28@bandit:~$ cd /tmp/tmp.e7BlmeyGE3

bandit28@bandit:/tmp/tmp.e7BlmeyGE3$ git clone ssh://bandit28-git@localhost:2220/home/bandit28-git/repo

Cloning into 'repo'...

The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.

ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.

This key is not known by any other names

Are you sure you want to continue connecting (yes/no/[fingerprint])? yes

Could not create directory '/home/bandit28/.ssh' (Permission denied).

Failed to add the host to the list of known hosts (/home/bandit28/.ssh/known_hosts).

                         _                     _ _ _   

                        | |__   __ _ _ __   __| (_) |_ 

                        | '_ \ / _` | '_ \ / _` | | __|

                        | |_) | (_| | | | | (_| | | |_ 

                        |_.__/ \__,_|_| |_|\__,_|_|\__|

  

                      This is an OverTheWire game server. 

            More information on http://www.overthewire.org/wargames

  

bandit28-git@localhost's password: 

remote: Enumerating objects: 9, done.

remote: Counting objects: 100% (9/9), done.

remote: Compressing objects: 100% (6/6), done.

remote: Total 9 (delta 2), reused 0 (delta 0), pack-reused 0

Receiving objects: 100% (9/9), done.

Resolving deltas: 100% (2/2), done.

bandit28@bandit:/tmp/tmp.e7BlmeyGE3$ ls -la

total 10564

drwx------    3 bandit28 bandit28     4096 Sep 23 04:28 .

drwxrwx-wt 4762 root     root     10801152 Sep 23 04:28 ..

drwxrwxr-x    3 bandit28 bandit28     4096 Sep 23 04:28 repo

bandit28@bandit:/tmp/tmp.e7BlmeyGE3$ cd repo/

bandit28@bandit:/tmp/tmp.e7BlmeyGE3/repo$ ls -la

total 16

drwxrwxr-x 3 bandit28 bandit28 4096 Sep 23 04:28 .

drwx------ 3 bandit28 bandit28 4096 Sep 23 04:28 ..

drwxrwxr-x 8 bandit28 bandit28 4096 Sep 23 04:28 .git

-rw-rw-r-- 1 bandit28 bandit28  111 Sep 23 04:28 README.md

bandit28@bandit:/tmp/tmp.e7BlmeyGE3/repo$ cat README.md 

# Bandit Notes

Some notes for level29 of bandit.

  

## credentials

  

- username: bandit29

- password: xxxxxxxxxx

  

bandit28@bandit:/tmp/tmp.e7BlmeyGE3/repo$ ls

README.md

bandit28@bandit:/tmp/tmp.e7BlmeyGE3/repo$ git branch -r -v

  origin/HEAD   -> origin/master

  origin/master 899ba88 fix info leak

bandit28@bandit:/tmp/tmp.e7BlmeyGE3/repo$ git status

On branch master

Your branch is up to date with 'origin/master'.

  

nothing to commit, working tree clean

bandit28@bandit:/tmp/tmp.e7BlmeyGE3/repo$ git checkout 899ba88

Note: switching to '899ba88'.

  

You are in 'detached HEAD' state. You can look around, make experimental

changes and commit them, and you can discard any commits you make in this

state without impacting any branches by switching back to a branch.

  

If you want to create a new branch to retain commits you create, you may

do so (now or later) by using -c with the switch command. Example:

  

  git switch -c <new-branch-name>

  

Or undo this operation with:

  

  git switch -

  

Turn off this advice by setting config variable advice.detachedHead to false

  

HEAD is now at 899ba88 fix info leak

bandit28@bandit:/tmp/tmp.e7BlmeyGE3/repo$ ls

README.md

bandit28@bandit:/tmp/tmp.e7BlmeyGE3/repo$ cat README.md 

# Bandit Notes

Some notes for level29 of bandit.

  

## credentials

  

- username: bandit29

- password: xxxxxxxxxx

  

bandit28@bandit:/tmp/tmp.e7BlmeyGE3/repo$ git status

HEAD detached at 899ba88

nothing to commit, working tree clean

bandit28@bandit:/tmp/tmp.e7BlmeyGE3/repo$ git log --oneline

899ba88 (HEAD, origin/master, origin/HEAD, master) fix info leak

abcff75 add missing data

c0a8c3c initial commit of README.md

bandit28@bandit:/tmp/tmp.e7BlmeyGE3/repo$ git restore .

bandit28@bandit:/tmp/tmp.e7BlmeyGE3/repo$ git status

HEAD detached at 899ba88

nothing to commit, working tree clean

bandit28@bandit:/tmp/tmp.e7BlmeyGE3/repo$ git checkout HEAD~1

Previous HEAD position was 899ba88 fix info leak

HEAD is now at abcff75 add missing data

bandit28@bandit:/tmp/tmp.e7BlmeyGE3/repo$ git checkout HEAD

bandit28@bandit:/tmp/tmp.e7BlmeyGE3/repo$ ls -la

total 16

drwxrwxr-x 3 bandit28 bandit28 4096 Sep 23 04:41 .

drwx------ 3 bandit28 bandit28 4096 Sep 23 04:28 ..

drwxrwxr-x 8 bandit28 bandit28 4096 Sep 23 04:41 .git

-rw-rw-r-- 1 bandit28 bandit28  133 Sep 23 04:41 README.md

bandit28@bandit:/tmp/tmp.e7BlmeyGE3/repo$ cat README.md 

# Bandit Notes

Some notes for level29 of bandit.

  

## credentials

  

- username: bandit29

- password: tQKvmcwNYcFS6vmPHIUSI3ShmsrQZK8S

  

bandit28@bandit:/tmp/tmp.e7BlmeyGE3/repo$
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
| ls | lista los archivos|
| cat| me muestra el contenido de un archivo|
## Referencias

git