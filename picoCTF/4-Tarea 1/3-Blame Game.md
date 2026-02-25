## Blame Game

### Descripción
Someone's commits seems to be preventing the program from working. Who is it?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/156/challenge.zip)
### Solución

#### Solución 1
Obtenemos con wget el archivo zip, y posteriormente con unzip lo descomprimimos.
```
DAVEst-picoctf@webshell:~$ ls 
challenge.zip  drop-in
DAVEst-picoctf@webshell:~$ cd drop-in/
DAVEst-picoctf@webshell:~/drop-in$ ls
message.py
DAVEst-picoctf@webshell:~/drop-in$ git log message.py
```

con git log message.py vemos el historial de commits y obtenemos: picoCTF{@sk_th3_1nt3rn_d2d29f22}
### Notas adicionales

### Referencias

-