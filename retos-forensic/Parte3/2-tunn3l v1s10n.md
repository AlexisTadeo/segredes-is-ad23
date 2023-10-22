### tunn3l v1s10n
## Objetivo

We found this [file](https://mercury.picoctf.net/static/01be2b38ba97802285a451b94505ea75/tunn3l_v1s10n). Recover the flag.
## Solución
```bash
- Descargamos el archivo
- le hacemos un file para saber que tipo de archivo es
- Nos damos cuenta que el archivo no tiene bien el encabezado
- Vamos a editar el encabezado
- Tiene que quedar de esta forma

00000000  42 4D 8E 26  2C 00 00 00   00 00 28 00  00 00 28 00                                                                                          BM.&,.....(...(.

- Con esto corregimos el error del archivo y podemos abrir la imagen
- Dentro de la imagen podemos ver un texto que nos dice "notaflag{sorry}"
- Inspeccionamos la imagen y parece ser muy chica para el peso de la imagen
- Le intentamos cambiar el alto de la imagen
- Cambiamos esta linea con el editor hexadecimal

00000010  00 00 6E 04  00 00 40 04   00 00 01 00  18 00 00 00                                                                                          ..n...@.........

- Con esto el alto de la imagen cambia y ya podemos observar la bandera al abrir la imagen
```
## Notas adicionales

## Bandera

picoCTF{qu1t3_a_v13w_2020}
## Hints

- Weird that it won't display right...