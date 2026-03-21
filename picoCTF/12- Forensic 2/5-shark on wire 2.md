## shark on wire 2

### Descripción
We found this [packet capture](https://challenge-files.picoctf.net/c_fickle_tempest/d2051a169bcab758191e43355c6954ae40a96b0791d75ad33737c7e9ca42703b/capture.pcap). Recover the flag.
### Solución

#### Solución 1
Intentamos abrir el archivo .pcap en Wireshark y buscar la bandera directamente en texto plano.
Recibimos tráfico de red aparentemente normal, pero la bandera no era visible porque estaba cifrada con TLS/HTTPS.
1. Abrimos el archivo de captura (.pcap) con Wireshark.
2. Identificamos el tráfico entre el cliente y el servidor, observando que utilizaban TLS.
3. Buscamos la clave de descifrado que normalmente se proporciona como pista en el reto.
4. Configuramos Wireshark para descifrar TLS usando la clave (Edit -> Preferences -> Protocols -> TLS).
5. Una vez descifrado el tráfico, examinamos los datos de la aplicación y encontramos la bandera en el cuerpo de una transmisión HTTP.
		picoCTF{sh4rk_w1th_s0m3_n3t_w1z_f593d6}
### Notas adicionales

### Referencias

-