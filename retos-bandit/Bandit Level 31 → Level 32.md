Bandit Level 31→ Level 32

## Objetivo

There is a git repository at `ssh://bandit31-git@localhost/home/bandit31-git/repo` via the port `2220`. The password for the user `bandit31-git` is the same as for the user `bandit31`.

Clone the repository and find the password for the next level.
## Datos de acceso al nivel

```
Usuario: bandit31
Contraseña: OoffzGDlzhAlerFJ2cAiz1D41JW1Mhmt
```
## Solución
```
Bash
bandit31@bandit:~$ mktemp -d

/tmp/tmp.8FNr0rGdYX

bandit31@bandit:~$ cd /tmp/tmp.8FNr0rGdYX

bandit31@bandit:/tmp/tmp.8FNr0rGdYX$ git clone ssh://bandit31-git@localhost:2220/home/bandit31-git/repo

Cloning into 'repo'...

The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.

ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.

This key is not known by any other names

Are you sure you want to continue connecting (yes/no/[fingerprint])? yes

Could not create directory '/home/bandit31/.ssh' (Permission denied).

Failed to add the host to the list of known hosts (/home/bandit31/.ssh/known_hosts).

                         _                     _ _ _   

                        | |__   __ _ _ __   __| (_) |_ 

                        | '_ \ / _` | '_ \ / _` | | __|

                        | |_) | (_| | | | | (_| | | |_ 

                        |_.__/ \__,_|_| |_|\__,_|_|\__|

  

                      This is an OverTheWire game server. 

            More information on http://www.overthewire.org/wargames

  

bandit31-git@localhost's password: 

remote: Enumerating objects: 4, done.

remote: Counting objects: 100% (4/4), done.

remote: Compressing objects: 100% (3/3), done.

remote: Total 4 (delta 0), reused 0 (delta 0), pack-reused 0

Receiving objects: 100% (4/4), done.

bandit31@bandit:/tmp/tmp.8FNr0rGdYX$ cd repo/

bandit31@bandit:/tmp/tmp.8FNr0rGdYX/repo$ ls -la

total 20

drwxrwxr-x 3 bandit31 bandit31 4096 Sep 23 05:16 .

drwx------ 3 bandit31 bandit31 4096 Sep 23 05:16 ..

drwxrwxr-x 8 bandit31 bandit31 4096 Sep 23 05:16 .git

-rw-rw-r-- 1 bandit31 bandit31    6 Sep 23 05:16 .gitignore

-rw-rw-r-- 1 bandit31 bandit31  147 Sep 23 05:16 README.md

bandit31@bandit:/tmp/tmp.8FNr0rGdYX/repo$ ls

README.md

bandit31@bandit:/tmp/tmp.8FNr0rGdYX/repo$ cat README.md 

This time your task is to push a file to the remote repository.

  

Details:

    File name: key.txt

    Content: 'May I come in?'

    Branch: master

  

bandit31@bandit:/tmp/tmp.8FNr0rGdYX/repo$ git log --oneline

362bfd5 (HEAD -> master, origin/master, origin/HEAD) initial commit

bandit31@bandit:/tmp/tmp.8FNr0rGdYX/repo$ git branch -rv

  origin/HEAD   -> origin/master

  origin/master 362bfd5 initial commit

bandit31@bandit:/tmp/tmp.8FNr0rGdYX/repo$ cat .gitignore

*.txt

bandit31@bandit:/tmp/tmp.8FNr0rGdYX/repo$ git ls-remote

The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.

ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.

This key is not known by any other names

Are you sure you want to continue connecting (yes/no/[fingerprint])? yes

Could not create directory '/home/bandit31/.ssh' (Permission denied).

Failed to add the host to the list of known hosts (/home/bandit31/.ssh/known_hosts).

                         _                     _ _ _   

                        | |__   __ _ _ __   __| (_) |_ 

                        | '_ \ / _` | '_ \ / _` | | __|

                        | |_) | (_| | | | | (_| | | |_ 

                        |_.__/ \__,_|_| |_|\__,_|_|\__|

  

                      This is an OverTheWire game server. 

            More information on http://www.overthewire.org/wargames

  

bandit31-git@localhost's password: 

From ssh://bandit31-git@localhost:2220/home/bandit31-git/repo

362bfd50c2007554b4aac93af07ebf964179a7b7 HEAD

362bfd50c2007554b4aac93af07ebf964179a7b7 refs/heads/master

bandit31@bandit:/tmp/tmp.8FNr0rGdYX/repo$ touch .gitkeep

bandit31@bandit:/tmp/tmp.8FNr0rGdYX/repo$ nano .gitkeep

Unable to create directory /home/bandit31/.local/share/nano/: No such file or directory

It is required for saving/loading search history or cursor positions.

  

bandit31@bandit:/tmp/tmp.8FNr0rGdYX/repo$ nano key.txt

Unable to create directory /home/bandit31/.local/share/nano/: No such file or directory

It is required for saving/loading search history or cursor positions.

  

bandit31@bandit:/tmp/tmp.8FNr0rGdYX/repo$ git status

On branch master

Your branch is up to date with 'origin/master'.

  

Untracked files:

  (use "git add <file>..." to include in what will be committed)

.gitkeep

  

nothing added to commit but untracked files present (use "git add" to track)

bandit31@bandit:/tmp/tmp.8FNr0rGdYX/repo$ rm .gitignore

bandit31@bandit:/tmp/tmp.8FNr0rGdYX/repo$ git status

On branch master

Your branch is up to date with 'origin/master'.

  

Changes not staged for commit:

  (use "git add/rm <file>..." to update what will be committed)

  (use "git restore <file>..." to discard changes in working directory)

deleted:    .gitignore

  

Untracked files:

  (use "git add <file>..." to include in what will be committed)

.gitkeep

key.txt

  

no changes added to commit (use "git add" and/or "git commit -a")

bandit31@bandit:/tmp/tmp.8FNr0rGdYX/repo$ git restore

fatal: you must specify path(s) to restore

bandit31@bandit:/tmp/tmp.8FNr0rGdYX/repo$ git restore .gitkeep

error: pathspec '.gitkeep' did not match any file(s) known to git

bandit31@bandit:/tmp/tmp.8FNr0rGdYX/repo$ git status

On branch master

Your branch is up to date with 'origin/master'.

  

Changes not staged for commit:

  (use "git add/rm <file>..." to update what will be committed)

  (use "git restore <file>..." to discard changes in working directory)

deleted:    .gitignore

  

Untracked files:

  (use "git add <file>..." to include in what will be committed)

.gitkeep

key.txt

  

no changes added to commit (use "git add" and/or "git commit -a")

bandit31@bandit:/tmp/tmp.8FNr0rGdYX/repo$ ls -la

total 24

drwxrwxr-x 3 bandit31 bandit31 4096 Sep 23 05:25 .

drwx------ 3 bandit31 bandit31 4096 Sep 23 05:16 ..

drwxrwxr-x 8 bandit31 bandit31 4096 Sep 23 05:26 .git

-rw-rw-r-- 1 bandit31 bandit31    8 Sep 23 05:23 .gitkeep

-rw-rw-r-- 1 bandit31 bandit31   15 Sep 23 05:24 key.txt

-rw-rw-r-- 1 bandit31 bandit31  147 Sep 23 05:16 README.md

bandit31@bandit:/tmp/tmp.8FNr0rGdYX/repo$ rm .gitkeep

bandit31@bandit:/tmp/tmp.8FNr0rGdYX/repo$ git status

On branch master

Your branch is up to date with 'origin/master'.

  

Changes not staged for commit:

  (use "git add/rm <file>..." to update what will be committed)

  (use "git restore <file>..." to discard changes in working directory)

deleted:    .gitignore

  

Untracked files:

  (use "git add <file>..." to include in what will be committed)

key.txt

  

no changes added to commit (use "git add" and/or "git commit -a")

bandit31@bandit:/tmp/tmp.8FNr0rGdYX/repo$ git add .

bandit31@bandit:/tmp/tmp.8FNr0rGdYX/repo$ git commit -m "xd"

[master 554a8ec] xd

 2 files changed, 1 insertion(+), 1 deletion(-)

 delete mode 100644 .gitignore

 create mode 100644 key.txt

bandit31@bandit:/tmp/tmp.8FNr0rGdYX/repo$ git push

The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.

ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY.

This key is not known by any other names

Are you sure you want to continue connecting (yes/no/[fingerprint])? yes

Could not create directory '/home/bandit31/.ssh' (Permission denied).

Failed to add the host to the list of known hosts (/home/bandit31/.ssh/known_hosts).

                         _                     _ _ _   

                        | |__   __ _ _ __   __| (_) |_ 

                        | '_ \ / _` | '_ \ / _` | | __|

                        | |_) | (_| | | | | (_| | | |_ 

                        |_.__/ \__,_|_| |_|\__,_|_|\__|

  

                      This is an OverTheWire game server. 

            More information on http://www.overthewire.org/wargames

  

bandit31-git@localhost's password: 

Enumerating objects: 4, done.

Counting objects: 100% (4/4), done.

Delta compression using up to 2 threads

Compressing objects: 100% (2/2), done.

Writing objects: 100% (3/3), 280 bytes | 280.00 KiB/s, done.

Total 3 (delta 0), reused 0 (delta 0), pack-reused 0

remote: ### Attempting to validate files... ####

remote: 

remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.

remote: 

remote: Well done! Here is the password for the next level:

remote: rmCBvG56y58BXzv98yZGdO7ATVL5dW8y 

remote: 

remote: .oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.oOo.

remote: 

To ssh://localhost:2220/home/bandit31-git/repo

 ! [remote rejected] master -> master (pre-receive hook declined)

error: failed to push some refs to 'ssh://localhost:2220/home/bandit31-git/repo'

bandit31@bandit:/tmp/tmp.8FNr0rGdYX/repo$
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
|- git add | agrega archivos para mandarlos al repositorio|
|- git commit | agrega un mensaje al push|
|- git push | manda los archivos al repositorio (hace un push)|
| ls | lista los archivos|
| cat| me muestra el contenido de un archivo|
## Referencias

git