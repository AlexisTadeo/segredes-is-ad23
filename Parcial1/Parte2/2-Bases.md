### Bases
## Objetivo

What does this `bDNhcm5fdGgzX3IwcDM1` mean? I think it has something to do with bases.
## Solución
```bash
alexistadeo2201-picoctf@webshell:~$ echo bDNhcm5fdGgzX3IwcDM1       
bDNhcm5fdGgzX3IwcDM1
alexistadeo2201-picoctf@webshell:~$ echo bDNhcm5fdGgzX3IwcDM1 | base32
MJCE42DDNU2WMZCHM55FQM2JO5RUITJRBI======
alexistadeo2201-picoctf@webshell:~$ echo bDNhcm5fdGgzX3IwcDM1 | base64 --decode
l3arn_th3_r0p35
alexistadeo2201-picoctf@webshell:~$ 
```
## Notas adicionales

| Comando | Descripción |
|-----------|-----------|
| echo | se encarga de escribir un string dado en salida estandar|
| base64 | codifica cadenas de caracteres|
|- base64 --decode | descodifica una cadena de caracteres codificada|
## Hints

- Submit your answer in our flag format. For example, if your answer was 'hello', you would submit 'picoCTF{hello}' as the flag.