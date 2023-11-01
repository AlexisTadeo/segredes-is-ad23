### Secrets
## Objetivo

We have several pages hidden. Can you find the one with the flag?The website is running [here](http://saturn.picoctf.net:64727/).
## Solución
```bash
- Entramos a la página.
- Al inspeccionar, vemos que existe una carpeta dentro llamada `/secrect/`, por lo que accedemos a ella.
- Volvemos a inspeccionar, y encontramos otra carpeta llamada `/hidden/`.
- Repetimos lo mismo, y encontramos otra carpeta `/superhidden/`.
- Al entrar ahí, volvemos a ver el código fuente, y encontraremos la bandera.
```
## Notas adicionales

## Bandera

picoCTF{succ3ss_@h3n1c@10n_790d2615}
## Hints

- folders folders folders
### Referencia