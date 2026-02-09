## Nice netcat...

### Descripción
There is a nice program that you can talk to by using this command in a shell:$ nc wily-courier.picoctf.net 63672, but it doesn't speak English...
### Solución

#### Solución 1
```
DAVEst-picoctf@webshell:~$ nc wily-courier.picoctf.net 63672
112 
105 
99 
111 
67 
84 
70 
123 
103 
48 
48 
100 
95 
107 
49 
116 
116 
121 
33 
95 
110 
49 
99 
51 
95 
107 
49 
116 
116 
121 
33 
95 
100 
53 
100 
56 
56 
125 
10 
```
https://www.duplichecker.com/ascii-to-text.php
Copíamos toda la saluda al link, y nos da como salida:
picoCTF{g00d_k1tty!_n1c3_k1tty!_d5d88}
### Notas adicionales

### Referencias

-