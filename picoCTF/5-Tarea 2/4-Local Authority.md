## Local Authority

### Descripción
Can you get the flag?

Additional details will be available after launching your challenge instance.
### Solución

#### Solución 1
Al ingresar a la página, iniciamos sesión y evidentemente nos dice que están mal los datos. Vemos el código fuente, y al ver el código de longin.php, vemos que hay otro archivo llamado secure.js, al entrar vemos que está el usuario y la contraseña representados así: 
if( username === 'admin' && password === 'strongPassword098765' )
  {
    return true;
  }

Al ingresar estos valores, nos arroja la bandera:

picoCTF{j5_15_7r4n5p4r3n7_b0c2c9cb}
### Notas adicionales

### Referencias

-