## Tab, Tab, Attack

### Descripción
Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames.[Addadshashanammu.zip](https://challenge-files.picoctf.net/c_wily_courier/ce53ef9432bf367be41e465224d721c1187c39debcd758efcd28e99a6b7ff7a4/Addadshashanammu.zip)
### Solución

#### Solución 1
```
DAVEst-picoctf@webshell:~$ cd Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
DAVEst-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/M
aelkashishi/Onnissiralis/Ularradallaku$ ls
fang-of-haynekhtnamet  fang-of-haynekhtnamet.c
DAVEst-picoctf@webshell:~/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/M
aelkashishi/Onnissiralis/Ularradallaku$ strings fang-of-haynekhtnamet | grep picoCTF
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_fc588427}
```
picoCTF{l3v3l_up!_t4k3_4_r35t!_fc588427}

### Notas adicionales
### Referencias

-