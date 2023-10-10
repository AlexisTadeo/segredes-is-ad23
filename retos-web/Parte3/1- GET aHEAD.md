### GET aHEAD
## Objetivo

Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:45028/](http://mercury.picoctf.net:45028/)
## Solución
```bash
1. Entrar a la pagina
2. Oprimir click derecho y oprimir inspeccionar
3. Seleccionar el encabezado de "Red"
4. Luego oprimir el boton "Choose Blue"
5. Seleccionar la llamada con comando de "POST"
6. De lado derecho, en el cuadro emergente oprimir "reenviar" o "Resend"
7. En el nuevo cuadro emergente en la parte superior izquierda cambiar el "POST" por "HEAD"
8. Luego en la parte de abajo de ese recuadro oprimimos enviar
9. Seleccionamos la nueva llamada que se hizo
10. Y en el apartado de "Encabezado de respuestas" estara la bandera
```
## Notas adicionales

- Este Programa tambien se puede realizar en la linea de comandos con el comando de "curl -I http://mercury.picoctf.net:45028/index.php"
- Tambien se puede realizar con proxies con el software de Kali
## Bandera

picoCTF{r3j3ct_th3_du4l1ty_775f2530}
## Hints

- Maybe you have more than 2 choices
- Check out tools like Burpsuite to modify your requests and look at the responses