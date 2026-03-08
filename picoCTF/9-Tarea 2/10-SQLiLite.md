## SQLiLite

### Descripción
Can you login to this website? Try to login [here](http://saturn.picoctf.net:58715/).
### Solución

#### Solución 1
Al ingresar en el login, nos dice que Login Failed. Y nos aparece la SQL Query que es la siguiente: SQL query: SELECT * FROM users WHERE name='a' AND password='a'. 
Por lo tanto lo único que tendremos que hacer es agregar despues del name lo siguente: ' --.

Y nos aparece Logged in! But can you see the flag, it is in plainsight. 
Vemos el código fuente y ahí está la bandera:

picoCTF{L00k5_l1k3_y0u_solv3d_it_ec8a64c7}

### Notas adicionales

### Referencias

-