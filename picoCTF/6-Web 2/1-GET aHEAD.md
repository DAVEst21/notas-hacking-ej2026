## GET aHEAD

### Descripción
Find the flag being held on this server to get ahead of the competition
### Solución

#### Solución 1
Entramos a la página y vemos que podemos cambiar el fondo entre rojo y azul. Al hacer click en los botones notamos que uno usa el método GET y el otro POST. El nombre del reto es “GET aHEAD”, entonces claramente no se trata solo de GET y POST. La pista dice que puede haber más de dos opciones, así que probamos con el método HEAD. Elegimos cualquier botón, le damos en resend y cambiamos el método a HEAD, enviamos la petición y en la respuesta aparece la flag.

picoCTF{r3j3ct_th3_du4l1ty_8b13f07}

#### Solución 2
También se puede hacer con Burp Suite. Instalamos FoxyProxy en el navegador y configuramos el proxy con el host y puerto de Burp. Luego en Burp nos vamos a Proxy → HTTP History, activamos Intercept y damos click en cualquier botón de la página. La petición se refleja en Burp, revisamos el response en HTTP History y ahí mismo aparece la bandera.

### Notas adicionales


### Referencias

-