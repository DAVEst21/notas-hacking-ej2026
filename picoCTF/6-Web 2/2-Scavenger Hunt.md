## Scavenger Hunt

### Descripción
There is some interesting information hidden around this site. Can you find it?

Additional details will be available after launching your challenge instance.
### Solución

#### Solución 1
Entramos al sitio y a simple vista no se ve nada raro, pero como el nombre dice “Scavenger Hunt”, básicamente es buscar cosas escondidas por todos lados. Primero revisamos el código fuente de la página principal y ahí encontramos una primera parte de la flag escondida en un comentario. Después empezamos a probar rutas interesantes que normalmente pueden contener información sensible. Probamos con `/robots.txt` y ahí encontramos otra pista que nos indicaba revisar otro archivo. Luego accedimos a `/.htaccess` y también a `/.DS_Store`, que son archivos que a veces quedan expuestos por mala configuración del servidor. Cada uno contenía partes adicionales de la bandera o pistas que llevaban a la siguiente ubicación. Finalmente también revisamos `index.php?` agregando parámetros a la URL, ya que en algunos retos esconden información en comentarios del código PHP o en parámetros especiales.

picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_9588550}
### Notas adicionales


### Referencias

-