### Irish-Name-Repo 3
## Objetivo

There is a secure website running at `https://jupiter.challenges.picoctf.org/problem/29132/` ([link](https://jupiter.challenges.picoctf.org/problem/29132/)) or http://jupiter.challenges.picoctf.org:29132. Try to see if you can login as admin!
## Solución
```bash
1. Entramos al link
2. Cliqueamos al menu de la parte superior izquierda
3. Entramos al adminLoggin
4. Inspeccionamos la pagina
5. Habilitamos la opcion debuger con 1
6. En el password le ponemos "'or1=1'"
7. Copiamos el password que nos da rotado
8. La pegamos en el password
9. Nos da la bandera
```
## Notas adicionales

Esta opcion tambien puede realizarce con la consola, usamos los mismos datos del problema anterior solo cambiamos los datos correspondientes, agregandole el encriptado de "ROT13" a la operacion de sql "'or1=1'"
## Bandera

picoCTF{3v3n_m0r3_SQL_06a9db19}
## Hints

- Seems like the password is encrypted.

## Referencia

https://www.w3schools.com/sql/sql_injection.asp

https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,13)&input=bnlya3ZmZ25xcmI