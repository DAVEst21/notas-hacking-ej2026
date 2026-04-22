## HideToSee

### Descripción
How about some hide and seek heh? Look at this image [here](https://artifacts.picoctf.net/c/236/atbash.jpg).
### Solución

#### Solución 1
```
sudo apt install steghide
steghide --extract -sf atbash.jpg
```

```
┌──(dave㉿kaliv1rus)-[~/picoctf/crypto]
└─$ cat encrypted.txt                                                            
krxlXGU{zgyzhs_xizxp_zx751vx6}
```
https://gchq.github.io/CyberChef/#recipe=Atbash_Cipher()&input=a3J4bFhHVXt6Z3l6aHNfeGl6eHBfeng3NTF2eDZ9
picoCTF{atbash_crack_ac751ec6}
### Notas adicionales
### Referencias

-