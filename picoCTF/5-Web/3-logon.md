## logon

### Descripción
The factory is hiding things from all of its users.Can you login as Joe and find what they've been looking at? http://fickle-tempest.picoctf.net:53486
### Solución

#### Solución 1
El sitio no permite iniciar sesión con el nombre de Joe, pero sí con cualquier otro valor.
Una vez dentro, instalamos la extensión Cookie-Editor para poder modificar los valores de las cookies, en este caso nos interesaba modificar el valor de Admin = False a True. Una vez guardada la nueva cookie, refrescamos la página y nos arroja la bandera.
picoCTF{th3_c0nsp1r4cy_l1v3s_4d184b0d}
### Notas adicionales

### Referencias

-