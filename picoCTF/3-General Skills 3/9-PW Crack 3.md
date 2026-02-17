## PW Crack 3

### Descripción
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/18/level3.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/18/level3.flag.txt.enc) and the [hash](https://artifacts.picoctf.net/c/18/level3.hash.bin) in the same directory too.There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.
### Solución

#### Solución 1
```
DAVEst-picoctf@webshell:~$ python level3.py 
Please enter correct password for flag: 8799
That password is incorrect
DAVEst-picoctf@webshell:~$ python level3.py 
Please enter correct password for flag: d3ab
That password is incorrect
DAVEst-picoctf@webshell:~$ python level3.py 
Please enter correct password for flag: 6f3d
That password is incorrect
DAVEst-picoctf@webshell:~$ python level3.py 
Please enter correct password for flag: a9de
That password is incorrect
DAVEst-picoctf@webshell:~$ python level3.py 
Please enter correct password for flag: 2295
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_6f98a49f}
```

picoCTF{m45h_fl1ng1ng_6f98a49f}
### Notas adicionales
- En el código venían cadenas que podían ser las correctas, intenté con las opciones hasta que me dio la bandera. Investigar otra manera de encontrar la bandera.
### Referencias

-