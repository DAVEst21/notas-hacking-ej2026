## picobrowser

### Descripción
This website can be rendered only by picobrowser, go and catch the flag!
### Solución

#### Solución 1
user-agent. Con inspeccionar vemos el apartado de network, al dar click en flag, vemos que el header en el user-agent tiene información de nuestro browser, el cual corresponde a Mozilla. Por lo tanto modificamos el user-agent a picobrowser, y volvemos a enviar la petición, y ahora nos da la bandera:
`picoCTF{p1c0_s3cr3t_ag3nt_fba5c48f}`
### Notas adicionales

### Referencias

-