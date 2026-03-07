## Roboto Sans

### Descripción
The flag is somewhere on this web application not necessarily on the website. Find it. Check [this](http://saturn.picoctf.net:58437/) out.
### Solución

#### Solución 1
Vemos en el título que tiene que ver con robots.txt, entonces vamos ahí y vemos esta cadena:
ZmxhZzEudHh0;anMvbXlmaW
anMvbXlmaWxlLnR4dA==
svssshjweuiwl;oiho.bsvdaslejg

nos vamos al cyberchef, y vemos línea por línea haber si tiene un auto-bake, y al introducir la segunda línea nos da la opción de bakear, y nos arroja: js/myfile.txt, entonces buscamos: http://saturn.picoctf.net:58437/js/myfile.txt y vemos la bandera:

picoCTF{Who_D03sN7_L1k5_90B0T5_718c9043}

https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=CmFuTXZiWGxtYVd4bExuUjRkQT09

### Notas adicionales

### Referencias

-