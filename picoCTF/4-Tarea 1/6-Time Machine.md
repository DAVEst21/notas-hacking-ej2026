## Time Machine

### Descripción
What was I last working on? I remember writing a note to help me remember...You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/160/challenge.zip)
### Solución

#### Solución 1
Obtenemos con wget el archivo zip, y posteriormente con unzip lo descomprimimos.
```
DAVEst-picoctf@webshell:~$ ls 
challenge.zip  drop-in
DAVEst-picoctf@webshell:~$ cd drop-in/
DAVEst-picoctf@webshell:~/drop-in$ ls
message.txt
DAVEst-picoctf@webshell:~/drop-in$ cat message.txt 
DAVEst-picoctf@webshell:~/drop-in$ git log
commit 89d296ef533525a1378529be66b22d6a2c01e530 (HEAD -> master)
Author: picoCTF <ops@picoctf.com>
Date:   Tue Mar 12 00:07:22 2024 +0000

    picoCTF{t1m3m@ch1n3_186cd7d7}
(END)
```
picoCTF{t1m3m@ch1n3_186cd7d7}
### Notas adicionales

### Referencias

-