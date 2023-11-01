### Packets Primer
## Objetivo

Download the packet capture file and use packet analysis software to find the flag.

- [Download packet capture](https://artifacts.picoctf.net/c/195/network-dump.flag.pcap)
## Solución
```bash
- Descargamos el archivo.
- Lo cargamos en la herramienta de Wireshark.
- Al primer paquete le damos en `follow/TCP stream`.
- En el primer paquete esta la bandera pero con espacios entre cada carácter.
- Se los quitamos manualmente y listo obtenemos la bandera.
```
## Notas adicionales

## Bandera

picoCTF{p4ck37_5h4rk_b9d53765}
## Hints

- Wireshark, if you can install and use it, is probably the most beginner friendly packet analysis software product.
### Referencia