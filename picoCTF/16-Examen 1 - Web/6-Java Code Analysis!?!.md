## Java Code Analysis!?!

### Descripción
BookShelf Pico, my premium online book-reading service. I believe that my website is super secure. I challenge you to prove me wrong by reading the 'Flag' book! Here are the credentials to get you started:

- Username: "user"
- Password: "user"

Source code can be downloaded [here](https://artifacts.picoctf.net/c/480/bookshelf-pico.zip). Website can be accessed [here!](http://saturn.picoctf.net:62612/).
### Solución

#### Solución 1
Las pistas de este problema nos mencionan que necesitamos modificar los JWT, para esto vamos a usar la herramienta https://www.jwt.io/.
Una vez que iniciamos sesión con las credenciales proporcionadas, vemos que con la extensión de cookie editor no vemos ninguna cookie. Por lo que vamos al inspector de almacenamiento local y vemos 2 token, uno con formato JWT y el otro de payload. Copiamos el auth-token y lo pegamos en la herramienta para modificar los valores a los siguientes:
	"role": "Admin",
	"userId": 2,
Además, es importante que la firma secreta sea 1234.
Una vez ingresado los valores, copiamos el JWT codificado, y lo pegamos en el auth-token. Además, modificamos los valores de role y userId, en el  payload, para que coincidan con el JWT.
Recargamos la página y damos click al libro "Flag", el cual tiene el siguiente contenido:

Great job! Here’s your flag:

picoCTF{w34k_jwt_n0t_g00d_7745dc02}

### Notas adicionales


### Referencias

-