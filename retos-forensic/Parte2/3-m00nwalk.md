### m00nwalk
## Objetivo

Decode this [message](https://jupiter.challenges.picoctf.org/static/fc1edf07742e98a480c6aff7d2546107/message.wav) from the moon.
## Solución
```bash
- Buscamos alguna herramienta en linea con la cual podamos decodificar la imagen que esta en formato de audio.
- Descargamos el [repositorio](https://github.com/colaclanth/sstv)
- Ejecutamos la siguiente linea de comando dentro de la carpeta del repositorio "python setup.py install"
- Luego en la carpeta donde tengamos el archivo que descargamos ejecutamos el siguiente comando:

- Con esto obtenemos la imagen que estaba codificada

┌──(kali㉿kali)-[~/picoctf/forensic/m00nwalk]
└─$ sstv -d message.wav -o result.png 
[sstv] Searching for calibration header... Found!    
[sstv] Detected SSTV mode Scottie 1
[sstv] Decoding image...   [###########################################] 100%
[sstv] Drawing image data...
[sstv] ...Done!
                                                                             
┌──(kali㉿kali)-[~/picoctf/forensic/m00nwalk]
└─$ ls
message.wav  result.png
```
## Notas adicionales

## Bandera

picoCTF{beep_boop_im_in_space}
## Hints

- How did pictures from the moon landing get sent back to Earth?
- What is the CMU mascot?, that might help select a RX option