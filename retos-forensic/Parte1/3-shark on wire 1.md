### shark on wire 1
## Objetivo

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/483e50268fe7e015c49caf51a69063d0/capture.pcap). Recover the flag.
## Solución
```bash
1. Descargamos el archivo
2. Lo abrimos con la aplicación wireshark de kali
3. Le damos clic derecho al primer UDP, le damos a follow y luego a UDP Stream
4. Esto nos mostrara lo que lleva cada UDP y nevegamos entre todas las UDP hasta encontrar la que contiene la bandera
```
## Notas adicionales

Wireshark es un analizador de protocolos utilizado para realizar análisis y solucionar problemas en redes de comunicaciones, para análisis de datos y protocolos, y como una herramienta didáctica.
## Bandera

picoCTF{StaT31355_636f6e6e}
## Hints

- Try using a tool like Wireshark
- What are streams?