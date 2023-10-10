### JaWT Scratchpad
## Objetivo

Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/61864/` or http://jupiter.challenges.picoctf.org:61864
## Solución
```bash
1. Entrar al link
2. Logearse con un nombre
3. Copear el token de la cookie que nos genera
4. Guardar el token en un documento hash
5. Si no se tiene instalar el paquete de john
6. Utilizar el documento hash con 'jonh hash -w-/usr/share/wordlist/rockyou.txt'
7. Pegar el token en la pagina https://jwt.io/
8. En el segundo apartado de la pagina cambiar el nombre por "admin"
9. En el tercer recuadro poner la palabra clave que sacamos anteriormente
10. Pegar en la cookie el nuevo token que nos dio la pagina
11. Guardar el nuevo token y recargar la pagina
12. Y listo
```
## Notas adicionales


## Bandera

picoCTF{jawt_was_just_what_you_thought_1ca14548}
## Hints

- What is that cookie?
- Have you heard of JWT?

## Referencias

https://jwt.io/
https://github.com/openwall/john