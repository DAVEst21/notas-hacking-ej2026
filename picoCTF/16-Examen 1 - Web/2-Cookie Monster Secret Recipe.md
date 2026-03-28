## Cookie Monster Secret Recipe

### Descripción
Cookie Monster has hidden his top-secret cookie recipe somewhere on his website. As an aspiring cookie detective, your mission is to uncover this delectable secret. Can you outsmart Cookie Monster and find the hidden recipe? You can access the Cookie Monster [here](http://verbal-sleep.picoctf.net:51625/) and good luck
### Solución

#### Solución 1 
Este problema se trata sobre las cookies, con las pistas podemos intuir que la extensión de cookie editor nos puede servir a resolver el problema.
Al ingresar a la página e iniciar sesión con usuario y contraseña de admin, nos dice que el acceso está denegado. Al ver las cookies con la extensión antes mencionada, notamos una cadena en base64, sin embargo al final de la cadena nos encontramos con '%3D%3D' lo cual nos dice que ahí tienen que ir 2 '=', entonces al agregar la cadena en cyberchef, nos decodifica la cadena:
https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=Y0dsamIwTlVSbnRqTURCck1XVmZiVEJ1YzNSbGNsOXNNSFpsYzE5ak1EQnJhV1Z6WHpRM016WkdOa05DZlE9PQ&oeol=CR

picoCTF{c00k1e_m0nster_l0ves_c00kies_4736F6CB}

### Notas adicionales

### Referencias

-