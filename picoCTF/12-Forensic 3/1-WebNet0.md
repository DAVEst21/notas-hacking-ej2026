## WebNet0

### Descripción
We found this [packet capture](https://challenge-files.picoctf.net/c_fickle_tempest/66113619363fca174ef6bf56587007af1626f99c44fc5cf92333f9fd8876ce9a/capture.pcap) and [key](https://challenge-files.picoctf.net/c_fickle_tempest/66113619363fca174ef6bf56587007af1626f99c44fc5cf92333f9fd8876ce9a/picopico.key). Recover the flag.
### Solución

#### Solución 1
Abrimos el archivo `.pcap` proporcionado por el desafío en Wireshark.

Al explorar la captura, notaremos que la mayoría de los paquetes son del protocolo TLS en el puerto 443. Si intentamos seguir un flujo TCP, veremos que los datos no son legibles porque están cifrados.

Necesitamos indicarle a Wireshark dónde está la clave privada para que pueda descifrar el tráfico TLS:

Vamos al menú **Edit** > **Preferences**. En la ventana de preferencias, desplegamos la sección **Protocols** en el panel izquierdo. Buscamos y seleccionamos **TLS** (o SSL en versiones antiguas). En la sección "RSA keys list", hacemos clic en **Edit...**. En la nueva ventana, hacemos clic en **New** para añadir una nueva entrada.

Configuramos los campos de la siguiente manera:

- **IP address:** `10.0.0.2` (esta es la IP del servidor en la captura)
    
- **Port:** `443`
    
- **Protocol:** `http`
    
- **Key File:** Hacemos clic en **Browse** y seleccionamos el archivo `.key` que descargamos del desafío
    
- **Password:** Lo dejamos en blanco
    

Aceptamos todas las ventanas con **OK**.

Una vez aplicada la configuración, notaremos un cambio inmediato en la captura: ahora aparecerán paquetes con el protocolo **HTTP** en lugar de solo TLS. En la columna de información, veremos peticiones como `GET /` y sus respuestas.

Para encontrar la flag, hacemos clic derecho en cualquier paquete HTTP que aparezca ahora. Seleccionamos **Follow** > **HTTP Stream**. Se abrirá una ventana con el contenido completo del flujo HTTP descifrado. Explorando el contenido, encontraremos la flag en el cuerpo de una de las respuestas.




### Notas adicionales
TLS es un protocolo criptográfico diseñado para proporcionar seguridad y privacidad en las comunicaciones a través de una red, principalmente Internet.



### Referencias

-