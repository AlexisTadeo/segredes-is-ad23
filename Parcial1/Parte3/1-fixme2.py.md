### fixme2.py
## Objetivo

Fix the syntax error in the Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/4/fixme2.py)
## Solución
```bash
alexistadeo2201-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/4/fixme2.py
--2023-10-01 21:54:57--  https://artifacts.picoctf.net/c/4/fixme2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.42, 3.160.5.18, 3.160.5.93, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.42|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1029 (1.0K) [application/octet-stream]
Saving to: 'fixme2.py'

fixme2.py                                          100%[==============================================================================================================>]   1.00K  --.-KB/s    in 0s      

2023-10-01 21:54:58 (337 MB/s) - 'fixme2.py' saved [1029/1029]

alexistadeo2201-picoctf@webshell:~$ nano fixme2.py
alexistadeo2201-picoctf@webshell:~$ python3 fixme2.py
That is correct! Here''s your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_e8814d03}
alexistadeo2201-picoctf@webshell:~$ 
```
## Notas adicionales

| Comando | Descripción |
## Hints

- Are equality and assignment the same symbol?
- To view the file in the webshell, do: `$ nano fixme2.py`
- To exit `nano`, press Ctrl and x and follow the on-screen prompts.
- The `str_xor` function does not need to be reverse engineered for this challenge.