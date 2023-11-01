### Local Authority
## Objetivo

Can you get the flag?Go to this [website](http://saturn.picoctf.net:50920/) and see what you can discover.
## Solución
```bash
- Entramos a la pagina web y la inspeccionamos.
- La pagina tiene una función PHP la cual verifica que el nombre de usuario y la contraseña solo puedan contener letras y números, además de comprobar el nombre de usuario y contraseña.
- El nombre de usuario y contraseña los comprueba a traves de una función JS en la cual se muestra el usuario y contraseña correctos.
- Con esto solo ponemos el usuario y contraseña que encontramos en el login y obtenemos la bandera.
```
## Notas adicionales

## Bandera

picoCTF{j5_15_7r4n5p4r3n7_05df90c8}
## Hints

- How is the password checked on this website?
### Referencia