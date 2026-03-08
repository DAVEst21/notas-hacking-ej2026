## IntroToBurp

### Descripción
Try [here](http://titan.picoctf.net:54634/) to find the flag
### Solución

#### Solución 1
Primero prendemos la intercepción del burp y el FoxyProxy, después de ingresar a la página y después de haber enviado el formulario, nos pide una clave de autenticación, al enviarla vemos que se envía una variable llamada OTP, la cual contiene el valor de la clave que introducimos. Lo que tenemos que hacer es borrar esa variable, porque así el sistema no tendrá ninguna variable a verificar por lo que se nos brindará el acceso a la siguiente página, dándonos así la bandera:

picoCTF{#0TP_Bypvss_SuCc3$S_6bffad21}

### Notas adicionales
Algo curioso que me demoró más tiempo en resolver el problema, es que yo eliminaba más lineas en el request, y al volver a enviarlo, se quedaba cargando. Es necesario no borrar líneas adicionales, ya que así no devuelve un response.

### Referencias

-