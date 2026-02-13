## Based

### Descripción
To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337?

Additional details will be available after launching your challenge instance.
### Solución

#### Solución 1
```
DAVEst-picoctf@webshell:~$ nc fickle-tempest.picoctf.net 63205
Let us see how data is stored
falcon
Please give the 01100110 01100001 01101100 01100011 01101111 01101110 as a word.
...
you have 45 seconds.....

Input:
falcon
Please give me the  o154 o151 o147 o150 o164 as a word.
Input:
light
Please give me the 706965 as a word.
Input:
pie
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_DF19A0E8}
```
Usamos cyberchef para realizar las operaciones. Para los valores en octal, usamos find and replace para quitar las 'o'.

- https://gchq.github.io/CyberChef/#recipe=Find_/_Replace(%7B'option':'Regex','string':'o'%7D,'',true,false,true,false)From_Octal('Space')&input=bzE1NCBvMTUxIG8xNDcgbzE1MCBvMTY0

picoCTF{learning_about_converting_values_DF19A0E8}

### Notas adicionales
- 1337 significa ser un experto en informática
### Referencias

-