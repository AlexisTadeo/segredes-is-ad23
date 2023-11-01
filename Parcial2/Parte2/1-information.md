### information
## Objetivo

Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://mercury.picoctf.net/static/d1375e383810d8d957c04eef9e345732/cat.jpg)
## Solución
```bash
alexistadeo2201-picoctf@webshell:~$ wget https://mercury.picoctf.net/static/7cf6a33f90deeeac5c73407a1bdc99b6/cat.jpg
--2023-10-23 17:44:47--  https://mercury.picoctf.net/static/7cf6a33f90deeeac5c73407a1bdc99b6/cat.jpg
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 878136 (858K) [application/octet-stream]
Saving to: 'cat.jpg'

cat.jpg                                      100%[============================================================================================>] 857.55K  1.86MB/s    in 0.5s    

2023-10-23 17:44:47 (1.86 MB/s) - 'cat.jpg' saved [878136/878136]

alexistadeo2201-picoctf@webshell:~$  exiftool cat.jpg 
ExifTool Version Number         : 12.40
File Name                       : cat.jpg
Directory                       : .
File Size                       : 858 KiB
File Modification Date/Time     : 2021:03:15 18:24:46+00:00
File Access Date/Time           : 2023:10:23 17:44:47+00:00
File Inode Change Date/Time     : 2023:10:23 17:44:47+00:00
File Permissions                : -rw-rw-r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.02
Resolution Unit                 : None
X Resolution                    : 1
Y Resolution                    : 1
Current IPTC Digest             : 7a78f3d9cfb1ce42ab5a3aa30573d617
Copyright Notice                : PicoCTF
Application Record Version      : 4
XMP Toolkit                     : Image::ExifTool 10.80
License                         : cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9
Rights                          : PicoCTF
Image Width                     : 2560
Image Height                    : 1598
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 2560x1598
Megapixels                      : 4.1
alexistadeo2201-picoctf@webshell:~$
```
## Notas adicionales

**ExifTool is a platform-independent [Perl library](https://exiftool.org/ExifTool.html) plus a [command-line application](https://exiftool.org/exiftool_pod.html) for reading, writing and editing meta information in a [wide variety of files](https://exiftool.org/#supported).** ExifTool supports many different metadata formats including [EXIF](https://exiftool.org/TagNames/EXIF.html), [GPS](https://exiftool.org/TagNames/GPS.html), [IPTC](https://exiftool.org/TagNames/IPTC.html), [XMP](https://exiftool.org/TagNames/XMP.html), [JFIF](https://exiftool.org/TagNames/JFIF.html), [GeoTIFF](https://exiftool.org/TagNames/GeoTiff.html), [ICC Profile](https://exiftool.org/TagNames/ICC_Profile.html), [Photoshop IRB](https://exiftool.org/TagNames/Photoshop.html), [FlashPix](https://exiftool.org/TagNames/FlashPix.html), [AFCP](https://exiftool.org/TagNames/AFCP.html) and [ID3](https://exiftool.org/TagNames/ID3.html), [Lyrics3](https://exiftool.org/TagNames/ID3.html#Lyrics3), as well as the maker notes of many digital cameras by [Canon](https://exiftool.org/TagNames/Canon.html), [Casio](https://exiftool.org/TagNames/Casio.html), [DJI](https://exiftool.org/TagNames/DJI.html), [FLIR](https://exiftool.org/TagNames/FLIR.html), [FujiFilm](https://exiftool.org/TagNames/FujiFilm.html), [GE](https://exiftool.org/TagNames/GE.html), [GoPro](https://exiftool.org/TagNames/GoPro.html), [HP](https://exiftool.org/TagNames/HP.html), [JVC/Victor](https://exiftool.org/TagNames/JVC.html), [Kodak](https://exiftool.org/TagNames/Kodak.html), [Leaf](https://exiftool.org/TagNames/Leaf.html), [Minolta/Konica-Minolta](https://exiftool.org/TagNames/Minolta.html), [Motorola](https://exiftool.org/TagNames/Motorola.html), [Nikon](https://exiftool.org/TagNames/Nikon.html), [Nintendo](https://exiftool.org/TagNames/Nintendo.html), [Olympus/Epson](https://exiftool.org/TagNames/Olympus.html), [Panasonic/Leica](https://exiftool.org/TagNames/Panasonic.html), [Pentax/Asahi](https://exiftool.org/TagNames/Pentax.html), [Phase One](https://exiftool.org/TagNames/PhaseOne.html), [Reconyx](https://exiftool.org/TagNames/Reconyx.html), [Ricoh](https://exiftool.org/TagNames/Ricoh.html), [Samsung](https://exiftool.org/TagNames/Samsung.html), [Sanyo](https://exiftool.org/TagNames/Sanyo.html), [Sigma/Foveon](https://exiftool.org/TagNames/Sigma.html) and [Sony](https://exiftool.org/TagNames/Sony.html).
## Bandera

picoCTF{the_m3tadata_1s_modified}
## Hints

- Look at the details of the file
- Make sure to submit the flag as picoCTF{XXXXX}

### Referencia