## rail-fence
### Descripción
A type of transposition cipher is the rail fence cipher, which is described [here](https://en.wikipedia.org/wiki/Rail_fence_cipher). Here is one such cipher encrypted using the rail fence with 4 rails. Can you decrypt it? Download the message [here](https://artifacts.picoctf.net/c/188/message.txt). Put the decoded message in the picoCTF flag format, `picoCTF{decoded_message}`.
### Solución

#### Solución 1
Utilicé la herramienta CyberChef con la función "Rail Fence Cipher Decode" y una clave de 4 rieles para descifrar el contenido del archivo `message.txt`. Al ser un cifrado de transposición, la frecuencia de letras se mantiene, pero el texto se vuelve legible al aplicar el patrón de zigzag correcto.
https://gchq.github.io/CyberChef/#recipe=Rail_Fence_Cipher_Decode(4,0)&input=VGEgXzdONkQ0OWhsZzpXM0RfSDNDMzFOX19BOTdlZiBzSFIwNTNGMzhONDNEN0IgaTMzX19fTjY
picoCTF{WH3R3_D035_7H3_F3NC3_8361N_4ND_3ND_4A76B997}

### Notas adicionales


### Referencias

-