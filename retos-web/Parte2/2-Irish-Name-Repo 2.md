### Irish-Name-Repo 2
## Objetivo

There is a website running at `https://jupiter.challenges.picoctf.org/problem/52849/` ([link](https://jupiter.challenges.picoctf.org/problem/52849/)). Someone has bypassed the login before, and now it's being strengthened. Try to see if you can still login! or http://jupiter.challenges.picoctf.org:52849
## Solución
```bash
1. Entramos al link
2. Cliqueamos al menu de la parte superior izquierda
3. Entramos al adminLoggin
4. Inspeccionamos la pagina
5. Habilitamos la opcion debuger con 1
6. En el username le ponemos "admin';", password "hola"
7. Nos da la bandera
```
## Notas adicionales

Esta opcion tambien puede realizarce con la consola, usamos los mismos datos del problema anterior solo cambiamos los datos correspondientes
## Bandera

picoCTF{m0R3_SQL_plz_fa983901}
## Hints

- The password is being filtered.

## Referencia

https://www.w3schools.com/sql/sql_injection.asp