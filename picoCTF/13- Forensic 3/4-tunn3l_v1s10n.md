## tunn3l_v1s10n

### Descripción
We found this file. Recover the flag.[tunn3l_v1s10n](https://challenge-files.picoctf.net/c_wily_courier/626df9feed926c1e1280804f5d87fde5576e266ff250a819a5528b0471b0f3f7/tunn3l_v1s10n)
### Solución

#### Solución 1
Abrimos el archivo en un visor de imágenes y notaremos que no se muestra correctamente, o que parece recortada o distorsionada.

Examinamos el archivo con un editor hexadecimal (como `xxd`, `hexedit`, o el visor hexadecimal de VSCode). Veremos la cabecera BMP y podremos observar que algo extraño ocurre con las dimensiones.

Un archivo BMP típico tiene la cabecera "BM" al inicio. Verificamos que esté presente. En este caso sí lo está, pero las dimensiones probablemente están modificadas.

Las dimensiones de un BMP se encuentran en los offsets:

- **0x12 (18 decimal):** Ancho de la imagen (4 bytes)
    
- **0x16 (22 decimal):** Alto de la imagen (4 bytes)
    

Notaremos que el alto de la imagen es un número muy grande o negativo. En BMP, el alto puede ser positivo (de abajo arriba) o negativo (de arriba abajo), pero aquí probablemente el valor está truncado o incorrecto.

Investigando un poco más, veremos que el campo "tamaño del archivo" en la cabecera tampoco coincide con el tamaño real.

Para corregir la imagen:

1. El ancho parece ser `0x0340` = 832 píxeles (correcto)
    
2. El alto es `0x32D` = 813 píxeles, pero el tamaño real del archivo sugiere que debería ser mayor. Probablemente el alto real debería ser `0x6A4` = 1700 píxeles (o un valor similar)
    

Cambiamos el valor del alto en el offset `0x16` al valor correcto (por ejemplo, `0x6A4` en little-endian sería `A4 06 00 00`).

Guardamos los cambios y abrimos la imagen nuevamente. Ahora veremos la imagen completa con la flag visible.
	picoCTF{qu1t3_a_v13w_2020}


### Notas adicionales

### Referencias

-