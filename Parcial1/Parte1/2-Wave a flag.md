### Wave a flag
## Objetivo
Can you invoke help flags for a tool or binary? [This program](https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm) has extraordinarily helpful information...
## Solución
```bash
alexistadeo2201-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm
alexistadeo2201-picoctf@webshell:~$ ls
warm
alexistadeo2201-picoctf@webshell:~$ ./warm
-bash: ./warm: Permission denied
alexistadeo2201-picoctf@webshell:~$ chmod +x warm
alexistadeo2201-picoctf@webshell:~$ ./warm
Hello user! Pass me a -h to learn what I can do!
alexistadeo2201-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_616f7182}
alexistadeo2201-picoctf@webshell:~$ 
```
## Notas adicionales

| Comando | Descripción |
|-----------|-----------|
| wget | descarga un archivo en la terminal|

## Hints

- This program will only work in the webshell or another Linux computer.

- To get the file accessible in your shell, enter the following in the Terminal prompt: `$ wget https://mercury.picoctf.net/static/beec4f433e5ee5bfcd71bba8d5863faf/warm`

- Run this program by entering the following in the Terminal prompt: `$ ./warm`, but you'll first have to make it executable with `$ chmod +x warm`

- -h and --help are the most common arguments to give to programs to get more information from them!

- Not every program implements help features like -h and --help.