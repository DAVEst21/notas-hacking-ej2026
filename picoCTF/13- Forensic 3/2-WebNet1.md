## WebNet1

### Descripción
We found this [packet capture](https://challenge-files.picoctf.net/c_fickle_tempest/d1e9add4e31989553f239ebf71ba5972f9bed7bd4932f931e14bfba80d75f815/capture.pcap) and [key](https://challenge-files.picoctf.net/c_fickle_tempest/d1e9add4e31989553f239ebf71ba5972f9bed7bd4932f931e14bfba80d75f815/picopico.key). Recover the flag.
### Solución

#### Solución 1 
Abrimos el archivo `.pcap` en Wireshark y configuramos la clave privada igual que en el desafío anterior:

Vamos a **Edit** > **Preferences** > **Protocols** > **TLS**. En "RSA keys list", hacemos clic en **Edit...** y luego en **New**. Configuramos:

- **IP address:** Lo dejamos en blanco
    
- **Port:** `443`
    
- **Protocol:** `http`
    
- **Key File:** Seleccionamos el archivo `.key` del desafío
    
- **Password:** En blanco
    

Aceptamos con **OK**.

Una vez aplicada la configuración, notaremos que el tráfico TLS ahora se muestra como HTTP descifrado.

Ahora viene la diferencia con WebNet0. Encontraremos una bandera falsa para despistarnos: `picoCTF{this.is.not.your.flag.anymore}`. Esta aparece en las cabeceras HTTP, pero no es la solución correcta.

Para encontrar la bandera real, necesitamos extraer los objetos HTTP:

1. Vamos a **File** > **Export Objects** > **HTTP**
    
2. Guardamos todos los archivos listados en una carpeta
    
3. Revisamos los archivos extraídos. Uno de ellos será `vulture.jpg`
    
4. Examinamos este archivo. La bandera no está visible a simple vista, sino que está oculta en los metadatos de la imagen
    

Para revelarla, podemos usar:

- **Hexdump:** `hexdump -C vulture.jpg | grep pico` (o simplemente examinar el hexdump completo)
    
- **Strings:** `strings vulture.jpg | grep pico`
    
- O abrir la imagen en un visor hexadecimal y buscar texto legible
    

Al inspeccionar los metadatos o el hexdump de `vulture.jpg`, encontraremos la bandera verdadera: 

`picoCTF{honey.roasted.peanuts}`

### Notas adicionales

### Referencias

-