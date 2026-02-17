## fixme2.py

### Descripción
Fix the syntax error in the Python script to print the flag.[Download Python script](https://artifacts.picoctf.net/c/5/fixme2.py)
### Solución

#### Solución 1
```
DAVEst-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/5/fixme2.py
--2026-02-17 00:09:13--  https://artifacts.picoctf.net/c/5/fixme2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.92, 3.160.22.43, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.92|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1029 (1.0K) [application/octet-stream]
Saving to: 'fixme2.py'

fixme2.py              100%[==========================>]   1.00K  --.-KB/s    in 0s      

2026-02-17 00:09:14 (294 MB/s) - 'fixme2.py' saved [1029/1029]

DAVEst-picoctf@webshell:~$ python fixme2.py 
  File "/home/DAVEst-picoctf/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
DAVEst-picoctf@webshell:~$ nano fixme2.py 
DAVEst-picoctf@webshell:~$ python fixme2.py 
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_4863e11b}
```

picoCTF{3qu4l1ty_n0t_4551gnm3nt_4863e11b}
### Notas adicionales

### Referencias

-