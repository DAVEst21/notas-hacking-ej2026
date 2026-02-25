## Collaborative Development

### Descripción
My team has been working very hard on new features for our flag printing program! I wonder how they'll work together?You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/176/challenge.zip)
### Solución

#### Solución 1
Obtenemos con wget el archivo zip, y posteriormente con unzip lo descomprimimos.
```
DAVEst-picoctf@webshell:~$ ls 
challenge.zip  drop-in
DAVEst-picoctf@webshell:~$ cd drop-in/
DAVEst-picoctf@webshell:~/drop-in$ ls
flag.py
DAVEst-picoctf@webshell:~/drop-in$ git log flag.py
```

No vemos nada...
```
DAVEst-picoctf@webshell:~/drop-in$ git branch -a
```
Vemos que hay 3 ramas locales diferentes...

```
$ git checkout feature/part-1
Switched to branch 'feature/part-1'

$ ls -al
total 16
drwxr-xr-x 3 shadownsa shadownsa 4096 Jan 30 12:30 .
drwxrwxr-x 4 shadownsa shadownsa 4096 Jan 30 12:24 ..
-rw-rw-r-- 1 shadownsa shadownsa   64 Jan 30 12:30 flag.py
drwxr-xr-x 8 shadownsa shadownsa 4096 Jan 30 12:30 .git

$ cat flag.py        
print("Printing the flag...")
print("picoCTF{t3@mw0rk_", end='') 
```

Obtenemos la primer parte de la bandera...
Hacemos lo mismo pero para las otras 3 partes.

```
DAVEst-picoctf@webshell:~/drop-in$ git checkout feature/part-2
Switched to branch 'feature/part-2'
DAVEst-picoctf@webshell:~/drop-in$ ls -al
total 12
drwxr-xr-x 3 DAVEst-picoctf DAVEst-picoctf   45 Feb 23 23:49 .
drwxr-xr-x 6 DAVEst-picoctf DAVEst-picoctf 4096 Feb 23 23:42 ..
drwxr-xr-x 8 DAVEst-picoctf DAVEst-picoctf 4096 Feb 23 23:49 .git
-rw-rw-r-- 1 DAVEst-picoctf DAVEst-picoctf   64 Feb 23 23:49 flag.py
DAVEst-picoctf@webshell:~/drop-in$ cat flag.py 
print("Printing the flag...")

print("m@k3s_th3_dr3@m_", end='')DAVEst-picoctf@webshell:~/drop-in$ git checkout feature/part-3
Switched to branch 'feature/part-3'
DAVEst-picoctf@webshell:~/drop-in$ ls -al
total 12
drwxr-xr-x 3 DAVEst-picoctf DAVEst-picoctf   45 Feb 23 23:50 .
drwxr-xr-x 6 DAVEst-picoctf DAVEst-picoctf 4096 Feb 23 23:42 ..
drwxr-xr-x 8 DAVEst-picoctf DAVEst-picoctf 4096 Feb 23 23:50 .git
-rw-rw-r-- 1 DAVEst-picoctf DAVEst-picoctf   55 Feb 23 23:50 flag.py
DAVEst-picoctf@webshell:~/drop-in$ cat flag.py 
print("Printing the flag...")

print("w0rk_2c91ca76}")
```
picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_2c91ca76}
### Notas adicionales

### Referencias

-