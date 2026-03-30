## Secret of the Polyglot

### Descripción
The Network Operations Center (NOC) of your local institution picked up a suspicious file, they're getting conflicting information on what type of file it is. They've brought you in as an external expert to examine the file. Can you extract all the information from this strange file? Download the suspicious file [here](https://artifacts.picoctf.net/c_titan/97/flag2of2-final.pdf).
### Solución

#### Solución 1
Al abrir el pdf, nos encontramos con la última parte de la flag:
1n_pn9_&_pdf_724b1287}

Después vimos los magibytes y vemos que el archivo es un png, entonces cambiamos la extensión a png, y al abrir la imagen nos da la primer parte de la flag
![[Pasted image 20260329213317.png]]

Aquí está el recorrido completo:
```
┌──(dave㉿kaliv1rus)-[~/picoctf/forensic/secretofthepolyglot]
└─$ open flag2of2-final.pdf                                                                                                                                           

┌──(dave㉿kaliv1rus)-[~/picoctf/forensic/secretofthepolyglot]
└─$ xxd -l 20 flag2of2-final.pdf 
00000000: 8950 4e47 0d0a 1a0a 0000 000d 4948 4452  .PNG........IHDR
00000010: 0000 0032                                ...2

┌──(dave㉿kaliv1rus)-[~/picoctf/forensic/secretofthepolyglot]
└─$ mv flag2of2-final.pdf flag2of2-final.png

┌──(dave㉿kaliv1rus)-[~/picoctf/forensic/secretofthepolyglot]
└─$ open flag2of2-final.png   
```

picoCTF{f1u3n7_1n_pn9_&_pdf_724b1287}
### Notas adicionales


### Referencias

-