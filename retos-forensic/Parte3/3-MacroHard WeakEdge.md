### MacroHard WeakEdge
## Objetivo

I've hidden a flag in this file. Can you find it? [Forensics is fun.pptm](https://mercury.picoctf.net/static/d3dd8cd51524d9fafcccd1b7d55f85e7/Forensics%20is%20fun.pptm)
## Solución
```bash
- Descargamos el archivo
- Nos dice que es un archivo de power point con una macro activada
- Desempaquetamos el archivo
- Abrimos la estructura del carpetas en visual code para explorar mejor los archivos
- Nos encontramos con un archivo que contiene una cadena en base 64
- Copiamos la cadena para convertirla en texto
- 
┌──(kali㉿kali)-[~/picoctf/forensic/MacroHardWeakEdge]
└─$ echo "Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q" | tr -d " " | base64 -d
flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}base64: invalid input
```
## Notas adicionales

## Bandera

picoCTF{D1d_u_kn0w_ppts_r_z1p5}
## Hints