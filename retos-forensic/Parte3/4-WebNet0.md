### WebNet0
## Objetivo

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.
## Solución
```bash
- Descargamos los dos archivos.
- Cargamos el archivo "capture.pcap" en wireshark.
- Como todos los paqutes estan encriptados no podemos ver su contenido.
- Cargamos el archivo "picopico.key" en la lista de protocolos/TLS/ y agregamos la llave.
- Con esto se desencriptan los paquetes y podemos hacer una búsqueda para encontrar la llave.
- Luego hacemos una búsqueda en los detalles de los paquetes buscando la cadena "picoCTF" y con esto encontramos la bandera.
```
## Notas adicionales

La Seguridad de la capa de transporte o TLS (Transport Layer Security en inglés) es un aspecto crucial de tu sitio web. Protege los datos de los usuarios de amenazas de seguridad como el malware y los ataques de denegación de servicio (DoS).

Disponer de TLS garantiza que sólo los usuarios autorizados puedan acceder a los datos mediante el cifrado. Por ejemplo, el uso de la encriptación TLS para una [tienda online](https://www.hostinger.es/tienda-online) asegurará las transacciones de tus clientes, convirtiendo sus datos sensibles en un código secreto. De este modo, terceros no podrán leer los datos.
## Bandera

picoCTF{nongshim.shrimp.crackers}
## Hints

- Try using a tool like Wireshark.
- How can you decrypt the TLS stream?

## Referencias

[¿Qué es TLS? Significado, uso y diferencias con SSL y HTTPS (hostinger.mx)](https://www.hostinger.mx/tutoriales/que-es-tls)