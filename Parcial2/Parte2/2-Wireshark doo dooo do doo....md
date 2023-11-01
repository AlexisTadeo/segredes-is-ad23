### Wireshark doo dooo do doo...
## Objetivo

Can you find the flag? [shark1.pcapng](https://mercury.picoctf.net/static/ae5b2bc07928fca272ff3900dc9a6cef/shark1.pcapng).
## Solución
```bash
- Descargamos el archivo.
- Lo cargamos en la herramienta de Wireshark.
- Ahí vemos que hay una conversación entre dos computadoras utilizando el protocolo HTTP.
- Damos click derecho sobre el primero, luego `follow/TCP stream`.
- Ahi vamos recorriendo entre la conversación buscando algo entre los paquetes que nos pueda servir.
- En el paquete numero 5 encontramos un texto que tiene el la apariencia de la bandera pero parece estar rotada.
- En la pagina `Cyberchef` y le aplicamos el filtro de rot13.
- Con esto obtenemos la bandera.
```
## Notas adicionales

## Bandera

picoCTF{p33kab00_1_s33_u_deadbeef}
## Hints

### Referencia

https://gchq.github.io/CyberChef/#recipe=A1Z26_Cipher_Decode('Space')&input=MTYgOSAzIDE1IDMgMjAgNiB7IDIwIDggNSAxNCAyMSAxMyAyIDUgMTggMTkgMTMgMSAxOSAxNSAxNCB9