### vault-door-5
## Objetivo

In the last challenge, you mastered octal (base 8), decimal (base 10), and hexadecimal (base 16) numbers, but this vault door uses a different change of base as well as URL encoding! The source code for this vault is here: [VaultDoor5.java](https://jupiter.challenges.picoctf.org/static/9505cca05dc00fecead41106370ee619/VaultDoor5.java)
## Solución
```bash
- Descargamos el archivo y lo abrimos.
- Copiamos el código cifrado y lo llevamos a [CyberChef]
- Lo decodificamos con base64 y URL decode.
- Obtenemos la contraseña.
```
## Notas adicionales

A URL is composed from a limited set of characters belonging to the US-ASCII character set. These characters include digits (0-9), letters(A-Z, a-z), and a few special characters (`"-"`, `"."`, `"_"`, `"~"`).
## Bandera

picoCTF{c0nv3rt1ng_fr0m_ba5e_64_84fd5095}
## Hints

- You may find an encoder/decoder tool helpful, such as https://encoding.tools/
- Read the wikipedia articles on URL encoding and base 64 encoding to understand how they work and what the results look like.

### Referencia

- [What is URL Encoding and How does it work? | URLEncoder](https://www.urlencoder.io/learn/)
- https://cyberchef.org/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)URL_Decode()&input=SlRZekpUTXdKVFpsSlRjMkpUTXpKVGN5SlRjMEpUTXhKVFpsSlRZM0pUVm0gSlRZMkpUY3lKVE13SlRaa0pUVm1KVFl5SlRZeEpUTTFKVFkxSlRWbUpUTTIKSlRNMEpUVm1KVE00SlRNMEpUWTJKVFkwSlRNMUpUTXdKVE01SlRNMQ