## interencdec

### Descripción
Can you get the real meaning from this file. Download the file [here](https://artifacts.picoctf.net/c_titan/109/enc_flag).
### Solución

#### Solución 1
```
┌──(dave㉿kaliv1rus)-[~/Documentos/notas-hacking-ej2026/Crypto]
└─$ cat enc_flag.1 
YidkM0JxZGtwQlRYdHFhR3g2YUhsZmF6TnFlVGwzWVROclgyMHdNakV5TnpVNGZRPT0nCg==

┌──(dave㉿kaliv1rus)-[~/Documentos/notas-hacking-ej2026/Crypto]
└─$ cat enc_flag.1 | base64 -d | tr -d "'b" | base64 -d                                                                                                               
wpjvJAM{jhlzhy_k3jy9wa3k_m0212758}

```
https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,19)&input=d3BqdkpBTXtqaGx6aHlfazNqeTl3YTNrX20wMjEyNzU4fQ
picoCTF{caesar_d3cr9pt3d_f0212758}
### Notas adicionales


### Referencias

-