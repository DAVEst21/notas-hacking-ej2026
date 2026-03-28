## head-dump

### Descripción
Welcome to the challenge! In this challenge, you will explore a web application and find an endpoint that exposes a file containing a hidden flag. The application is a simple blog website where you can read articles about various topics, including an article about API Documentation. Your goal is to explore the application and find the endpoint that generates files holding the server’s memory, where a secret flag is hidden. The website is running [picoCTF News](http://verbal-sleep.picoctf.net:61459/).
### Solución

#### Solución 1
La descripción del problema nos dice que debemos encontrar la aplicación de la API en donde encontraremos un artefacto que nos genera un archivo donde la bandera está oculta. 
Viendo el código fuente de la página web con ctrl-F buscando la palabra API, encontramos un href que nos puede servir:
```
<!-- Message -->
<div class="mb-4">
    <p class="text-gray-800">Explore backend development with us <a href="" class="text-blue-600">#nodejs</a> ,
        <a href="" class="text-blue-600">#swagger UI</a> , <a href="/api-docs" class="text-blue-600 hover:underline">#API Documentation</a> 
    </p>
</div>
```
Ponemos en el navegador el `/api-docs` y ahora nos encontramos en la aplicación que nos comentaban en la descripción del problema. En el último apartado se encuentra un botón para probar el funcionamiento del GET/heapdump y nos dice: Diagnosing the memory allocation. Al darle click nos aparece un link para descargar el archivo, y en la terminal buscamos la palabra 'picoCTF{':
```
┌──(dave㉿kaliv1rus)-[~/Descargas]
└─$ cat heapdump-1774647347248.heapsnapshot | grep picoCTF{
picoCTF{Pat!3nt_15_Th3_K3y_a485f162}

```
picoCTF{Pat!3nt_15_Th3_K3y_a485f162}

### Notas adicionales


### Referencias

-