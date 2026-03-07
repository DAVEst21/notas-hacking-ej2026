## SOAP

### Descripción
The web project was rushed and no security assessment was done. Can you read the /etc/passwd file?

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
JSON es más ligero, rápido y legible, ideal para APIs y aplicaciones modernas, mientras que XML es más verboso pero superior en validación de datos complejos y documentos estructurados
. JSON usa pares clave-valor (formato llave {}), mientras que XML usa etiquetas (<tag>). JSON es el estándar preferido hoy por su simplicidad.

### Referencias

-