## extensions

### Descripción
This is a really weird text file. Can you find the flag? Get the flag from [TXT](https://challenge-files.picoctf.net/c_fickle_tempest/31fe772e6a4c71e867af0b2a93818e06d8f8ebf8af2a9615495d00356ff576da/flag.txt).
### Solución

#### Solución 1
Con xxd -l 20 flag.txt vemos por los magic bits que es un png, entonces con mv cambiamos la extensión a png y nos da la bandera:

picoCTF{now_you_know_about_extensions}

### Notas adicionales

### Referencias

-