### WebNet1
## Objetivo

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key). Recover the flag.
## Solución
```bash
- Descargamos los dos archivos.
- Realizamos los mismos pasos que en WebNet0.
- Con esto desencriptamos algunos paquetes.
- Nos damos cuenta que se esta descargando una imagen.
- La extraemos con la opción de "export objects" de wireshark.
- La guardamos y vamos a examinar la imagen.
- Al abrir la imagen nos damos cuenta que ahí no hay nada.
- Le aplicamos un strings y ahí es donde se encuentra la bandera.

┌──(kali㉿kali)-[~/picoctf/forensic/WebNet1]
└─$ strings vulture.jpg | grep "picoCTF"
picoCTF{honey.roasted.peanuts}
```
## Notas adicionales

## Bandera

picoCTF{honey.roasted.peanuts}
## Hints

- Try using a tool like Wireshark.
- How can you decrypt the TLS stream?