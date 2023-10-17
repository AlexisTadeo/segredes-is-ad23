### So Meta
## Objetivo

Find the flag in this [picture](https://jupiter.challenges.picoctf.org/static/916b07b4c87062c165ace1d3d31ef655/pico_img.png).
## Solución
```bash
alexistadeo2201-picoctf@webshell:~$ wget https://jupiter.challenges.picoctf.org/static/916b07b4c87062c165ace1d3d31ef655/pico_img.png
--2023-10-17 02:05:05--  https://jupiter.challenges.picoctf.org/static/916b07b4c87062c165ace1d3d31ef655/pico_img.png
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 108795 (106K) [application/octet-stream]
Saving to: 'pico_img.png'

pico_img.png                                       100%[==============================================================================================================>] 106.25K  --.-KB/s    in 0.05s   

2023-10-17 02:05:05 (2.21 MB/s) - 'pico_img.png' saved [108795/108795]

alexistadeo2201-picoctf@webshell:~$ strings pico_img.png | grep "pico"
picoCTF{s0_m3ta_d8944929}K
alexistadeo2201-picoctf@webshell:~$ 
```
## Notas adicionales


## Bandera

picoCTF{s0_m3ta_d8944929}
## Hints

- What does meta mean in the context of files?
- Ever heard of metadata?