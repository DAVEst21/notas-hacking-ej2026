## strings it

### Descripción
Can you find the flag in [file](https://challenge-files.picoctf.net/c_fickle_tempest/fd00e7cc9b263f22c323572d2d5fc37d170f8e58e99a91f8991d0f07c69b21ff/strings) without running it?
### Solución

#### Solución 1
```
DAVEst-picoctf@webshell:~$ strings strings | grep picoCTF
picoCTF{5tRIng5_1T_FB7D7Bb6}
```
Los archivos elf generalmente se ejecutan, pero el ejecutarlo no era la sol. Entonces obtenemos las cadenas del archivo y filtramos las que tengan 'picoCTF'.

picoCTF{5tRIng5_1T_FB7D7Bb6}
### Notas adicionales
### Referencias

-