## Bookmarklet

### Descripción
Why search for the flag when I can make a bookmarklet to print it for me? Browse [here](http://titan.picoctf.net:50464/), and find the flag!
### Solución

#### Solución 1
La tercer pista nos dice: "Web browsers have other ways to run JavaScript too.", entonces se asume que se va a ejecutar un script en la consola de la página web.
Al ingresar a la página copiamos el 'bookmarklet' que se nos proporciona y lo pegamos en la consola:
```
        javascript:(function() {
            var encryptedFlag = "àÒÆÞ¦È¬ëÙ£ÖÓÚåÛÑ¢ÕÓ¨ÍÕÄ¦í";
            var key = "picoctf";
            var decryptedFlag = "";
            for (var i = 0; i < encryptedFlag.length; i++) {
                decryptedFlag += String.fromCharCode((encryptedFlag.charCodeAt(i) - key.charCodeAt(i % key.length) + 256) % 256);
            }
            alert(decryptedFlag);
        })();
```
La página nos da como salida una alerta con la bandera:

picoCTF{p@g3_turn3r_18d2fa20}



### Notas adicionales


### Referencias

-