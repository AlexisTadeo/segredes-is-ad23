### runme.py
## Objetivo

Run the `runme.py` script to get the flag. Download the script with your browser or with `wget` in the webshell.[Download runme.py Python script](https://artifacts.picoctf.net/c/34/runme.py)
## Solución
```bash
alexistadeo2201-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/34/runme.py
--2023-10-01 22:16:44--  https://artifacts.picoctf.net/c/34/runme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.42, 3.160.5.71, 3.160.5.93, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.42|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 270 [application/octet-stream]
Saving to: 'runme.py'

runme.py                                           100%[==============================================================================================================>]     270  --.-KB/s    in 0s      

2023-10-01 22:16:44 (78.5 MB/s) - 'runme.py' saved [270/270]

alexistadeo2201-picoctf@webshell:~$ ./runme.py
-bash: ./runme.py: Permission denied
alexistadeo2201-picoctf@webshell:~$ chmod +x runme.py 
alexistadeo2201-picoctf@webshell:~$ ./runme.py
picoCTF{run_s4n1ty_run}
alexistadeo2201-picoctf@webshell:~$ 
```
## Notas adicionales

| Comando | Descripción |
## Hints

- If you have Python on your computer, you can download the script normally and run it. Otherwise, use the `wget`command in the webshell.
- To use `wget` in the webshell, first right click on the download link and select 'Copy Link' or 'Copy Link Address'
- Type everything after the dollar sign in the webshell: `$ wget` , then paste the link after the space after `wget` and press enter. This will download the script for you in the webshell so you can run it!
- Finally, to run the script, type everything after the dollar sign and then press enter: `$ python3 runme.py` You should have the flag now!