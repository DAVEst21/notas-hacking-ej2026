## Matryoshka doll

### Descripción
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one?Image: [dolls.jpg](https://challenge-files.picoctf.net/c_wily_courier/f1f4181c217358672b720e801df28731166311181fd73b364baa4479f8500044/dolls.jpg)
### Solución

#### Solución 1
Ejecutamos `binwalk dolls.jpg` para ver qué archivos están ocultos dentro de la imagen. Veremos que hay varios archivos ZIP incrustados.

Extraemos los archivos con:

```
binwalk -e dolls.jpg
```

Esto creará una carpeta llamada `_dolls.jpg.extracted`. Dentro de ella, encontraremos una nueva imagen (probablemente `base_images/2_c.jpg` o similar) y posiblemente un archivo ZIP.

Notaremos que este proceso se repite: cada vez que extraemos una imagen, dentro hay otra imagen oculta. Es como abrir una muñeca rusa tras otra.

Seguimos extrayendo cada imagen con `binwalk -e` hasta que ya no encontremos más archivos incrustados.

En la última extracción, en lugar de otra imagen, encontraremos un archivo de texto con la flag.
	picoCTF{e3f378fe6c1ea7f6bc5ac2c3d6801c1f}




### Notas adicionales


### Referencias

-