### fixme1.py
## Objetivo

Fix the syntax error in this Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/27/fixme1.py)
## Solución
```bash
alexistadeo2201-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/27/fixme1.py
--2023-10-01 21:36:41--  https://artifacts.picoctf.net/c/27/fixme1.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.71, 3.160.5.93, 3.160.5.42, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.71|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 837 [application/octet-stream]
Saving to: 'fixme1.py'

fixme1.py                                          100%[==============================================================================================================>]     837  --.-KB/s    in 0s      

2023-10-01 21:36:41 (317 MB/s) - 'fixme1.py' saved [837/837]

alexistadeo2201-picoctf@webshell:~$ nano fixme1.py
alexistadeo2201-picoctf@webshell:~$ python3 fixme1.py
That is correct! Here''s your flag: picoCTF{1nd3nt1ty_cr1515_182342f7}
alexistadeo2201-picoctf@webshell:~$ 
```
## Notas adicionales

| Comando | Descripción |
## Hints

- Indentation is very meaningful in Python
- To view the file in the webshell, do: `$ nano fixme1.py`
- To exit `nano`, press Ctrl and x and follow the on-screen prompts.
- The `str_xor` function does not need to be reverse engineered for this challenge.
