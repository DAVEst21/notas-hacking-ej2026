## plumbing

### Descripción
Sometimes you need to handle process data outside of a file. Can you find a way to keep the output from this program and search for the flag?Connect to fickle-tempest.picoctf.net 54542.
### Solución

#### Solución 1
```
DAVEst-picoctf@webshell:~$ nc fickle-tempest.picoctf.net 54542 > aaa.txt
DAVEst-picoctf@webshell:~$ grep "picoCTF" aaa.txt
picoCTF{digital_plumb3r_00da27CC}
```

picoCTF{digital_plumb3r_00da27CC}
### Notas adicionales

### Referencias

-