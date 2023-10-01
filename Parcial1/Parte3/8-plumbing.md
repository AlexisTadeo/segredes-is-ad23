### plumbing
## Objetivo

Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag? Connect to `jupiter.challenges.picoctf.org 4427`.
## Solución
```bash
alexistadeo2201-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 4427 | grep pico
picoCTF{digital_plumb3r_5ea1fbd7}

alexistadeo2201-picoctf@webshell:~$ 
```
## Notas adicionales

| Comando | Descripción |
## Hints

- Remember the flag format is picoCTF{XXXX}
- What's a pipe? No not that kind of pipe... This [kind](http://www.linfo.org/pipes.html)