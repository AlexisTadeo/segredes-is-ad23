### Mind your Ps and Qs
## Objetivo

In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/b9ddda080c56fb421bf30409bec3460d/values)
## Solución
```bash
alexistadeo2201-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/b9ddda080c56fb421bf30409bec3460d/values
--2023-11-01 16:17:59--  https://mercury.picoctf.net/static/b9ddda080c56fb421bf30409bec3460d/values
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 206 [application/octet-stream]
Saving to: 'values'

values                                             100%[==============================================================================================================>]     206  --.-KB/s    in 0s      

2023-11-01 16:17:59 (99.9 MB/s) - 'values' saved [206/206]

alexistadeo2201-picoctf@webshell:~$ ls
_dolls.jpg.extracted  values
alexistadeo2201-picoctf@webshell:~$ cat values 
Decrypt my super sick RSA:
c: 964354128913912393938480857590969826308054462950561875638492039363373779803642185
n: 1584586296183412107468474423529992275940096154074798537916936609523894209759157543
e: 65537alexistadeo2201-picoctf@webshell:~$ python3
Python 3.10.6 (main, Aug 10 2022, 11:40:04) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> exit
Use exit() or Ctrl-D (i.e. EOF) to exit
>>> exit()
alexistadeo2201-picoctf@webshell:~$ python3
Python 3.10.6 (main, Aug 10 2022, 11:40:04) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> c = 964354128913912393938480857590969826308054462950561875638492039363373779803642185
>>> n = 1584586296183412107468474423529992275940096154074798537916936609523894209759157543
>>> e = 65537
>>> p = 2434792384523484381583634042478415057961
>>> q = 650809615742055581459820253356987396346063
>>> t = (p-1)*(q-1)
>>> d = pow(e,-1,t)
>>> m = pow(c,d,n)
>>> m
13016382529449106065927291425342535437996222135352905256639684640304028661985917
>>> bytes.fromhex(hex(m)[2:]).decode()
'picoCTF{sma11_N_n0_g0od_73918962}'
```
## Notas adicionales

## Bandera

picoCTF{sma11_N_n0_g0od_73918962}
## Hints

- Bits are expensive, I used only a little bit over 100 to save money
### Referencia

http://factordb.com/index.php?query=1584586296183412107468474423529992275940096154074798537916936609523894209759157543