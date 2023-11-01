### Forbidden Paths
## Objetivo

Can you get the flag?Here's the [website](http://saturn.picoctf.net:55793/).We know that the website files live in `/usr/share/nginx/html/` and the flag is at `/flag.txt` but the website is filtering absolute file paths. Can you get past the filter to read the flag?
## Solución
```bash
- Entramos a la página, y vemos que podemos colocar texto en un recuadro.
- Regresamos en la ruta utilizando `../../../../flag.txt` y obtenemos la bandera.
```
## Notas adicionales

## Bandera

picoCTF{7h3_p47h_70_5ucc355_e5a6fcbc}
## Hints

### Referencia