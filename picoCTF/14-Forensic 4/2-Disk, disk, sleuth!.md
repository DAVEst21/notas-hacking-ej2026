## Disk, disk, sleuth!

### Descripción
Use `srch_strings` from the sleuthkit and some terminal-fu to find a flag in this disk image. [dds1-alpine.flag.img.gz](https://challenge-files.picoctf.net/c_wily_courier/a7895bbce833fd95502d3a661fa54735e90d9bec9346d711ff05cbd40b5f3c8e/dds1-alpine.flag.img.gz)
### Solución

#### Solución 1 
Descargamos y descomprimimos la imagen de disco:

```
gunzip dds1-alpine.flag.img.gz
```

Usamos `srch_strings` de Sleuthkit para buscar cadenas de texto en la imagen:

```
srch_strings -a dds1-alpine.flag.img | grep picoCTF
```

Obtendremos la flag directamente:

picoCTF{f0r3ns1c4t0r_n30phyt3_ad5c96c0}
### Notas adicionales

### Referencias

-