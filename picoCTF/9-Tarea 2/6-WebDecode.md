## WebDecode

### Descripción
Do you know how to use the web inspector? Start searching [here](http://titan.picoctf.net:54597/) to find the flag
### Solución

#### Solución 1
Vemos la página y siempre nos dice que usemos el inspector, al entrar al apartado de ABOUT, vemos en inspeccionar que hay un notify_true="cGljb0NURnt3ZWJfc3VjYzNzc2Z1bGx5X2QzYzBkZWRfMDJjZGNiNTl9", esto está en base64, vamos al cyberchef y nos da la bandera:

picoCTF{web_succ3ssfully_d3c0ded_02cdcb59}

https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=Y0dsamIwTlVSbnQzWldKZmMzVmpZek56YzJaMWJHeDVYMlF6WXpCa1pXUmZNREpqWkdOaU5UbDk
### Notas adicionales

### Referencias

-