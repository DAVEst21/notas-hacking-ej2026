## Operation Oni

### Descripción
Download this disk image, find the key and log into the remote machine. Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

Additional details will be available after launching your challenge instance.
### Solución

#### Solución 1
Descargamos y descomprimimos la imagen de disco.

Analizamos la tabla de particiones con `fdisk`:

```
fdisk -l disk.img
```

Identificamos el offset de la partición Linux. Calculamos el offset en bytes (sector de inicio × 512).

Creamos un directorio y montamos la partición:

```
mkdir /mnt/disk
mount -o loop,ro,offset=<offset> disk.img /mnt/disk
```

Buscamos claves SSH en el sistema de archivos:

```
find /mnt/disk -name "*id*" 2>/dev/null
```

Encontraremos una clave privada en `/root/.ssh/id_ed25519` o similar.

Extraemos la clave:

```
cp /mnt/disk/root/.ssh/id_ed25519 .
chmod 600 id_ed25519
```

Usamos la clave para conectarnos al servicio remoto:

```
ssh -i id_ed25519 -p <puerto> ctf-player@saturn.picoctf.net
```

Una vez dentro, obtendremos la flag.

### Notas adicionales


### Referencias

-