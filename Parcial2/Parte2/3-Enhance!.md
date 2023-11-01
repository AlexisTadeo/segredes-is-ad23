### Enhance!
## Objetivo

Download this image file and find the flag.

- [Download image file](https://artifacts.picoctf.net/c/100/drawing.flag.svg)
## Solución
```bash
┌──(kali㉿kali)-[~/Downloads]
└─$ strings drawing.flag.svg | grep "tspan"
       id="text3723"><tspan
         id="tspan3748">p </tspan><tspan
         id="tspan3754">i </tspan><tspan
         id="tspan3756">c </tspan><tspan
         id="tspan3758">o </tspan><tspan
         id="tspan3760">C </tspan><tspan
         id="tspan3762">T </tspan><tspan
         id="tspan3764">F { 3 n h 4 n </tspan><tspan
         id="tspan3752">c 3 d _ a a b 7 2 9 d d }</tspan></text>
                                                                                  
┌──(kali㉿kali)-[~/Downloads]
└─$
```
## Notas adicionales

## Bandera

picoCTF{3nh4nc3d_aab729dd}
## Hints

### Referencia