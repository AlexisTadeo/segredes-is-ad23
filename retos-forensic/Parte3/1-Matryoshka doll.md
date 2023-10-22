### Matryoshka doll
## Objetivo

Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/2978e1270538613cd8181c7b0dabe9bd/dolls.jpg)
## Solución
```bash
alexistadeo2201-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/2978e1270538613cd8181c7b0dabe9bd/dolls.jpg
--2023-10-22 05:29:12--  https://mercury.picoctf.net/static/2978e1270538613cd8181c7b0dabe9bd/dolls.jpg
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 651622 (636K) [application/octet-stream]
Saving to: 'dolls.jpg'

dolls.jpg                                          100%[==============================================================================================================>] 636.35K  1.87MB/s    in 0.3s    

2023-10-22 05:29:12 (1.87 MB/s) - 'dolls.jpg' saved [651622/651622]

alexistadeo2201-picoctf@webshell:~$ binwalk dolls.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 594 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378942, uncompressed size: 383937, name: base_images/2_c.jpg
651600        0x9F150         End of Zip archive, footer length: 22

alexistadeo2201-picoctf@webshell:~$ binwalk -e dolls.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 594 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
272492        0x4286C         Zip archive data, at least v2.0 to extract, compressed size: 378942, uncompressed size: 383937, name: base_images/2_c.jpg
651600        0x9F150         End of Zip archive, footer length: 22

alexistadeo2201-picoctf@webshell:~$ cd _dolls.jpg.extracted 
alexistadeo2201-picoctf@webshell:~/_dolls.jpg.extracted$ cd base_images
alexistadeo2201-picoctf@webshell:~/_dolls.jpg.extracted/base_images$ binwalk -e 2_c.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 526 x 1106, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
187707        0x2DD3B         Zip archive data, at least v2.0 to extract, compressed size: 196042, uncompressed size: 201444, name: base_images/3_c.jpg
383804        0x5DB3C         End of Zip archive, footer length: 22
383915        0x5DBAB         End of Zip archive, footer length: 22

alexistadeo2201-picoctf@webshell:~/_dolls.jpg.extracted/base_images$ cd _2_c.jpg.extracted/base_images
alexistadeo2201-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images$ binwalk -e 3_c.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 428 x 1104, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
123606        0x1E2D6         Zip archive data, at least v2.0 to extract, compressed size: 77650, uncompressed size: 79806, name: base_images/4_c.jpg
201422        0x312CE         End of Zip archive, footer length: 22

alexistadeo2201-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images$ cd _3_c.jpg.extracted/base_images
alexistadeo2201-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images$ binwalk -e 4_c.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 320 x 768, 8-bit/color RGBA, non-interlaced
3226          0xC9A           TIFF image data, big-endian, offset of first image directory: 8
79578         0x136DA         Zip archive data, at least v2.0 to extract, compressed size: 62, uncompressed size: 81, name: flag.txt
79784         0x137A8         End of Zip archive, footer length: 22

alexistadeo2201-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images$ cd _4_c.jpg.extracted/
alexistadeo2201-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted$ ls
136DA.zip  flag.txt
alexistadeo2201-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted$ cat flag.txt 
picoCTF{4cf7ac000c3fb0fa96fb92722ffb2a32}alexistadeo2201-picoctf@webshell:~/_dolls.jpg.extracted/base_images/_2_c.jpg.extracted/base_images/_3_c.jpg.extracted/base_images/_4_c.jpg.extracted$ 
```
## Notas adicionales

## Bandera

picoCTF{4cf7ac000c3fb0fa96fb92722ffb2a32}
## Hints

- Wait, you can hide files inside files? But how do you find them?
- Make sure to submit the flag as picoCTF{XXXXX}
