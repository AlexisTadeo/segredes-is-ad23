### vault-door-1
## Objetivo

This vault uses some complicated arrays! I hope you can make sense of it, special agent. The source code for this vault is here: [VaultDoor1.java](https://jupiter.challenges.picoctf.org/static/87e103a8db01087de9ccf5a7a022ddf8/VaultDoor1.java)
## Solución
```bash
- Descargamos el archivo y lo abrimos.
- Vemos que la bandera esta desordenada en la comparison.
- Editamos el archivo para que en cada línea existan 2 dígitos para ordenarlos.

┌──(kali㉿kali)-[~/picoctf/reverse/vault-door-1]
└─$ cat bandera | sort | awk '{print($3)}' | tr -d "'" | tr -d "\n"
d35cr4mbl3_tH3_cH4r4cT3r5_f6daf4;                                                                                  
┌──(kali㉿kali)-[~/picoctf/reverse/vault-door-1]
└─$ 

- Y con esto ya tendríamos la bandera.
```
## Notas adicionales

## Bandera

picoCTF{d35cr4mbl3_tH3_cH4r4cT3r5_f6daf4}
## Hints

- Look up the charAt() method online.

### Referencia