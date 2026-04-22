## Pixelated

### Descripción
I have these 2 images, can you make a flag out of them? [scrambled1.png](https://challenge-files.picoctf.net/c_wily_courier/948209c9bfbe84d9dce56e1bbd6d7eb768730f7ad07bc425c493f224d0e47ccf/scrambled1.png) [scrambled2.png](https://challenge-files.picoctf.net/c_wily_courier/948209c9bfbe84d9dce56e1bbd6d7eb768730f7ad07bc425c493f224d0e47ccf/scrambled2.png)### Solución

#### Solución 1
```
cd /opt 
sudo wget http://www.caesum.com/handbook/Stegsolve.jar -O stegsolve.jar 
sudo chmod +x stegsolve.jar 
java -jar /opt/stegsolve.jar
```
- Abrimos la primer imagen
    
    - `File - Open`
    
- La combinamos con la segunda
    
    - `Analyse - Image Combiner`
    
- Usamos los iconos de flecha en la parte de abajo para elegir el tipo de combinación hasta encontrar AND

#### Solución 2
```
from PIL import Image
import numpy as np

imagen1 = np.asarray( Image.open('scrambled1.png') )
imagen2 = np.asarray( Image.open('scrambled2.png') )

data = imagen1 + imagen2

nueva = Image.fromarray(data)
nueva.save("out.png", "PNG")
```

![[Pasted image 20260422080300.png]]
### Notas adicionales
La criptografía visual es una técnica de cifrado que permite codificar información visual de manera que la información descifrada se presente como una imagen visual. Una de las técnicas más reconocidas fue desarrollada por Moni Naor y Adi Shamir en 1994. ​
### Referencias

-