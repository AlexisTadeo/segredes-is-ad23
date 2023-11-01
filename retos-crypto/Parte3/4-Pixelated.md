### Pixelated
## Objetivo

I have these 2 images, can you make a flag out of them? [scrambled1.png](https://mercury.picoctf.net/static/49743139fb7c10765dbf462d40987d2a/scrambled1.png) [scrambled2.png](https://mercury.picoctf.net/static/49743139fb7c10765dbf462d40987d2a/scrambled2.png)
## Solución
```bash
from PIL import Image
import numpy as np

imagen1 = np.asarray(Image.open('scrambled1.png'))
imagen2 = np.asarray(Image.open('scrambled2.png'))

data = imagen1 + imagen2

nueva = Image.fromarray(data)

nueva.save('lachida.png','PNG')

#picoCTF{2a4d45c7}
```
## Notas adicionales

## Bandera

picoCTF{2a4d45c7}
## Hints

- [https://en.wikipedia.org/wiki/Visual_cryptography](https://en.wikipedia.org/wiki/Visual_cryptography)
- Think of different ways you can "stack" images
### Referencia

https://imagemagick.org/index.php
