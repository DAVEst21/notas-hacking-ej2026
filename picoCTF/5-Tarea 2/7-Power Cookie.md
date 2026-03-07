## Power Cookie

### Descripción
Can you get the flag? Go to this [website](http://saturn.picoctf.net:56857/) and see what you can discover.
### Solución

#### Solución 1
La pista nos dice que si sabemos modificar cookies, pues claro que sí!
Hacemos click al botón de continuar como guest, pero no nos da la bandera, vemos la extensión de Cookie-Editor, y vemos que hay una cookie llamada isAdmin con valor en 0, entonces la modificamos a 1, y nos da la bandera:

picoCTF{gr4d3_A_c00k13_5d2505be}
### Notas adicionales

### Referencias

-