## Secrets

### Descripción
We have several pages hidden. Can you find the one with the flag? The website is running [here](http://saturn.picoctf.net:63533/).
### Solución

#### Solución 1
Vemos el código fuente, vemos que hay cosas que están en .../secret/, entonces ponemos: http://saturn.picoctf.net:63533/secret/, y al inspeccionar vemos que hay un hidden/ ... entonces vamos a http://saturn.picoctf.net:63533/secret/hidden/ y al inspeccionar vemos que hay un superhidden/ y al ingresar a http://saturn.picoctf.net:63533/secret/hidden/superhidden/ vemos que dice "Finally. You found me. But can you see me" y al ver el código fuente vemos la bandera:

picoCTF{succ3ss_@h3n1c@10n_39849bcf}

### Notas adicionales

### Referencias

-