## Milkslap

### Descripción
🥛
### Solución

#### Solución 1
Abrimos el enlace proporcionado en el desafío y notaremos que la página muestra una animación similar a [eelslap.com](https://eelslap.com/). Inspeccionando el código fuente, encontramos una referencia a un archivo `concat_v.png` en el CSS.

Descargamos este archivo y verificamos sus dimensiones con:


```
file concat_v.png
```

Notaremos que tiene una altura inusualmente grande: 47520 píxeles, lo que sugiere que contiene múltiples imágenes concatenadas.

Usamos `zsteg`, una herramienta específica para esteganografía en PNG:

```
zsteg -s first concat_v.png
```

En la salida, encontraremos la flag oculta en uno de los canales:

picoCTF{imag3_m4n1pul4t10n_sl4p5}

### Notas adicionales



### Referencias

-