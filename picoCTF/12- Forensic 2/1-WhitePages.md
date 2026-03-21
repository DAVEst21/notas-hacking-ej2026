## WhitePages

### Descripción
I stopped using YellowPages and moved onto WhitePages... but [the page they gave me](https://challenge-files.picoctf.net/c_fickle_tempest/4de4b105d28cb6df34d9805217f2460b978a37dafc3dfc50edadd8d424dd311a/whitepages.txt) is all blank!
### Solución

#### Solución 1
Recibimos un archivo que al abrirlo no mostraba información visible, pero al inspeccionarlo con un editor que revela caracteres ocultos, descubrimos que contenía espacios, tabulaciones y saltos de línea en patrones inusuales.

1. Copiamos y pegamos el contenido del archivo en un editor que muestra caracteres ocultos o utilizamos una herramienta de análisis de whitespace (como Snowflake).
2. Identificamos que los espacios, las tabulaciones y los saltos de línea se usaban como código binario, donde un patrón de caracteres (espacio = 0, tabulación = 1) codificaba datos binarios.
3. Decodificamos la secuencia binaria a texto ASCII.
4. La decodificación reveló la bandera.
	picoCTF{n0t_a_s1mpl3_sp4c3_934d7d}


### Notas adicionales


### Referencias

-