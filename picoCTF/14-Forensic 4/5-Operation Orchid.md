## Operation Orchid

### Descripción
Download this disk image and find the flag. Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/213/disk.flag.img.gz)
### Solución

#### Solución 1
Descargamos y descomprimimos la imagen de disco.

Montamos la imagen para examinar su contenido. Primero, analizamos las particiones con `mmls` y calculamos el offset.

Montamos la partición:

```
mount -o loop,ro,offset=<offset> disk.img /mnt
```

Explorando el sistema de archivos, encontraremos un archivo cifrado con AES-256. Notaremos que junto al archivo hay una clave o pista.

Usamos OpenSSL para descifrar el archivo:

```
openssl enc -aes-256-cbc -d -in encrypted_file -out decrypted_file -pass pass:<clave>
```

La flag aparecerá en el archivo descifrado.

picoCTF{orchid_flag_here}
### Notas adicionales


### Referencias

-