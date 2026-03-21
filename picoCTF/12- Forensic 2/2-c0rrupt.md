## c0rrupt

### Descripción
We found this [file](https://challenge-files.picoctf.net/c_fickle_tempest/87bdc8ce30b177d033b3d68bca4647950bb07304032861baa912ebe08701d355/mystery). Recover the flag.
### Solución

#### Solución 1 
Recibimos un error de apertura o una imagen que no se mostraba correctamente, indicando que el archivo estaba corrupto o dañado.

1. Abrimos el archivo con un editor hexadecimal (hexedit, HxD o el visor hexadecimal de VSCode).
2. Comparamos el encabezado del archivo corrupto con el encabezado estándar para ese tipo de archivo (por ejemplo, los primeros bytes de un PNG deben ser 89 50 4E 47).
3. Detectamos que uno o más bytes en la firma del archivo estaban incorrectos o que algún campo de longitud estaba mal escrito.
4. Corregimos manualmente el byte corrupto en el editor hexadecimal.
5. Guardamos el archivo corregido y lo abrimos normalmente para ver la imagen que contenía la bandera.
		picoCTF{h3x_3d1t1ng_fTw_85e0c4}
### Notas adicionales

### Referencias

-