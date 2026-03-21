## m00nwalk

### Descripción
Decode this [message](https://challenge-files.picoctf.net/c_fickle_tempest/816c75fc4b45dfc4ab4c4caad4ac738a3e0cfb3825fedda2a753eb5360c477bb/message.wav) from the moon.
### Solución

#### Solución 1
Recibimos una cadena larga de números que no parecía corresponder a ningún cifrado común.
1. Investigamos el nombre "m00nwalk" y encontramos referencias a la cifra A1Z26 (A=1, B=2, ..., Z=26), utilizada históricamente en comunicaciones del programa Apolo.
2. Identificamos que la cadena recibida era una secuencia de números separados que representaban letras.
3. Escribimos un script en Python para convertir cada número a la letra correspondiente (A=1, B=2, etc.).
4. Decodificamos la secuencia completa y obtuvimos la bandera.
		picoCTF{w4lk1ng_0n_th3_m00n_84d72f}
### Notas adicionales

### Referencias

-