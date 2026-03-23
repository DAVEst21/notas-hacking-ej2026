## Sleuthkit Apprentice

### Descripción
Download this disk image and find the flag. Note: if you are using the webshell, download and extract the disk image into `/tmp` not your home directory.

- [Download compressed disk image](https://artifacts.picoctf.net/c/138/disk.flag.img.gz)
### Solución

#### Solución 1
Descargamos y descomprimimos la imagen:

```
wget https://artifacts.picoctf.net/c/336/disk.flag.img.gz
gunzip disk.flag.img.gz
```

Analizamos la tabla de particiones con `mmls`:

```
mmls disk.flag.img
```

Notaremos que hay una partición Linux. Listamos los archivos de esa partición con `fls` usando el offset correspondiente:

```
fls -o <offset> disk.flag.img -r | grep flag
```

Encontraremos un archivo `flag.txt` que aparece como eliminado (marcado con `*` o `-`). Recuperamos su contenido con `icat` usando el inodo:

```
icat -o <offset> disk.flag.img <inode>
```

Obtendremos la flag:

picoCTF{by73_5urf3r_25b0d0c0}

### Notas adicionales

### Referencias

-