## Cookies

### Descripción
Who doesn't love cookies? Try to figure out the best one.
### Solución

#### Solución 1 y 2
Al entrar a la página vemos que si ponemos nombres de galletas normales nos dice que no es una cookie válida. Si ponemos **snickerdoodle**, que es la sugerencia que aparece, vemos que sí es válida, pero dice que no es la mejor. Entonces abrimos el cookie-editor del navegador y revisamos el valor de la cookie llamada `name`, vemos que tiene valor 0. La cambiamos a 1, recargamos y ahora nos muestra otro nombre de cookie. Si seguimos cambiando el valor (2, 3, 4, etc.) vamos obteniendo diferentes respuestas, así que claramente la flag está en alguno de esos valores. En vez de hacerlo manualmente uno por uno, abrimos la terminal y usamos un pequeño loop con curl para probar varios valores automáticamente:

```
┌──(dave㉿kaliv1rus)-[~]
└─$ for i in {1..30}; do curl -s http://wily-courier.picoctf.net:53217/check -H "Cookie: name=$i"; done | grep pico
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_a4dadb49}

```

picoCTF{3v3ry1_l0v3s_c00k135_a4dadb49}
### Notas adicionales
Este reto es para entender que las cookies se pueden modificar del lado del cliente y que muchas veces el servidor solo está validando el valor que recibe.

### Referencias

-