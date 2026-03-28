## findme

### Descripción
Help us test the form by submiting the username as `test` and password as `test!` The website running [here](http://saturn.picoctf.net:61274/).
### Solución

#### Solución 1
Abrimos burpsuite para ver si encontramos algo. Al iniciar sesión con las credenciales de test para usuario y test! para contraseña, vemos que el url nos aparece como http://saturn.picoctf.net:49714/next-page/id=cGljb0NURntwcm94aWVzX2Fs, vemos que la cadena está codificada. Al poner esta primer cadena en cyberchef (https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=Y0dsamIwTlVSbnR3Y205NGFXVnpYMkZz&oeol=CR) obtenemos lo siguiente: "picoCTF{proxies_al". Al volver a darle click en enviar en el BurpSuite, vemos que obtenemos otra cadena interesante para ingresar en cyberchef: http://saturn.picoctf.net:49714/next-page/id=bF90aGVfd2F5XzAxZTc0OGRifQ== (https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=YkY5MGFHVmZkMkY1WHpBeFpUYzBPR1JpZlE9PQ&oeol=CR) y obtenemos la otra mitad de la bandera: "l_the_way_01e748db}"

picoCTF{proxies_all_the_way_01e748db}


### Notas adicionales

### Referencias

-