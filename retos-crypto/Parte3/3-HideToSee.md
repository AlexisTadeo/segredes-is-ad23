### HideToSee
## Objetivo

How about some hide and seek heh?Look at this image [here](https://artifacts.picoctf.net/c/239/atbash.jpg).
## Solución
```bash
alexistadeo2201-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/239/atbash.jpg
--2023-11-01 18:36:07--  https://artifacts.picoctf.net/c/239/atbash.jpg
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.5.18, 3.160.5.42, 3.160.5.93, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.5.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 51504 (50K) [application/octet-stream]
Saving to: 'atbash.jpg'

atbash.jpg                                     100%[=================================================================================================>]  50.30K  --.-KB/s    in 0.02s   

2023-11-01 18:36:08 (2.50 MB/s) - 'atbash.jpg' saved [51504/51504]

alexistadeo2201-picoctf@webshell:~$ ls                          
README.txt  _dolls.jpg.extracted  atbash.jpg  values
alexistadeo2201-picoctf@webshell:~$ steghide extract -sf atbash.jpg
Enter passphrase: 
wrote extracted data to "encrypted.txt".
alexistadeo2201-picoctf@webshell:~$ ls    
README.txt  _dolls.jpg.extracted  atbash.jpg  encrypted.txt  values
alexistadeo2201-picoctf@webshell:~$ cat encrypted.txt 
krxlXGU{zgyzhs_xizxp_1u84w779}
alexistadeo2201-picoctf@webshell:~$

- Atbash Cipher
```
## Notas adicionales

## Bandera

picoCTF{atbash_crack_1f84d779}
## Hints

- Download the image and try to extract it.
### Referencia

https://gchq.github.io/CyberChef/