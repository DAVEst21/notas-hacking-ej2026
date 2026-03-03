## JaWT Scratchpad

### Descripción
There is some interesting information hidden around this site. Can you find it?

Additional details will be available after launching your challenge instance.
### Solución

#### Solución 1
El payload decodificado mostraba algo como:
```
{  
	"user": "guest"  
}
```
Se cambió a:
```
{  
	"user": "admin"  
}
```
El reto utilizaba un secreto débil o conocido (por ejemplo: `ilovepico`).

Se generó un nuevo token firmado correctamente con el secret correcto.

Al reemplazar la cookie con el nuevo JWT → se obtuvo acceso privilegiado.

picoCTF{jawt_was_just_what_you_thought_bbb82bd4a57564aefb32d69dafb60583}
### Notas adicionales


### Referencias

-