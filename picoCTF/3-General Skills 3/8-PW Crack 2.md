## PW Crack 2

### Descripción
Can you crack the password to get the flag?Download the password checker [here](https://artifacts.picoctf.net/c/13/level2.py) and you'll need the encrypted [flag](https://artifacts.picoctf.net/c/13/level2.flag.txt.enc) in the same directory too.
### Solución

#### Solución 1
```
DAVEst-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/13/level2.py
--2026-02-17 00:15:22--  https://artifacts.picoctf.net/c/13/level2.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.43, 3.160.22.128, 3.160.22.92, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.43|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 914 [application/octet-stream]
Saving to: 'level2.py'

level2.py              100%[==========================>]     914  --.-KB/s    in 0s      

2026-02-17 00:15:22 (378 MB/s) - 'level2.py' saved [914/914]

DAVEst-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/13/level2.flag.txt.enc
--2026-02-17 00:15:30--  https://artifacts.picoctf.net/c/13/level2.flag.txt.enc
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.128, 3.160.22.92, 3.160.22.43, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.128|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 31 [application/octet-stream]
Saving to: 'level2.flag.txt.enc'

level2.flag.txt.enc    100%[==========================>]      31  --.-KB/s    in 0s      

2026-02-17 00:15:30 (19.1 MB/s) - 'level2.flag.txt.enc' saved [31/31]

DAVEst-picoctf@webshell:~$ nano level2.py 
DAVEst-picoctf@webshell:~$ python level2.py 
Please enter correct password for flag: dde76
That password is incorrect
DAVEst-picoctf@webshell:~$ nano level2.py 
DAVEst-picoctf@webshell:~$ python level2.py 
Please enter correct password for flag: de76
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_489dea9a}
```

picoCTF{tr45h_51ng1ng_489dea9a}

https://gchq.github.io/CyberChef/#recipe=From_Hex('0x')&input=MHg2NDB4NjUweDM3MHgzNg
### Notas adicionales

### Referencias

-