## Sleuthkit Intro

### Descripción
Download the disk image and use `mmls` on it to find the size of the Linux partition. Connect to the remote checker service to check your answer and get the flag. Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory. [Download disk image](https://artifacts.picoctf.net/c/164/disk.img.gz)

Additional details will be available after launching your challenge instance.
### Solución

#### Solución 1
Descargamos y descomprimimos la imagen de disco proporcionada.

Ejecutamos `mmls` para listar las particiones:

```
mmls disk.img
```

Identificamos la partición Linux (generalmente la partición 4 o la de mayor tamaño). Notaremos el valor en la columna "Length" (en sectores).

Nos conectamos al servicio remoto con netcat:

```
nc saturn.picoctf.net <puerto>
```

Ingresamos la longitud de la partición Linux en sectores y obtendremos la flag.

### Notas adicionales


### Referencias

-