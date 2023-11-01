### Redaction gone wrong
## Objetivo

Now you DON’T see me.This [report](https://artifacts.picoctf.net/c/84/Financial_Report_for_ABC_Labs.pdf) has some critical data in it, some of which have been redacted correctly, while some were not. Can you find an important key that was not redacted properly?
## Solución
```bash
- Descargamos el archivo, y resulta que es un PDF.
- El PDF contiene palabras subrayadas, pero algunas se pueden seleccionar.
- Entre las palabras selecciona-bles se encuentra la bandera.
```
## Notas adicionales

## Bandera

picoCTF{C4n_Y0u_S33_m3_fully}
## Hints

- How can you be sure of the redaction?
### Referencia