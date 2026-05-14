## credstuff
#### Descripción 
We found a leak of a blackmarket website's login credentials. Can you find the password of the user `cultiris` and successfully decrypt it? Download the leak [here](https://artifacts.picoctf.net/c/151/leak.tar). The first user in `usernames.txt` corresponds to the first password in `passwords.txt`. The second user corresponds to the second password, and so on.
#### Solución

```
┌──(dave㉿kaliv1rus)-[~/picoctf/crypto]
└─$ tar -xf leak.tar.1

┌──(dave㉿kaliv1rus)-[~/picoctf/crypto]
└─$ ls                                                                           
a               creedstuff     leak.tar.1     readmycert.csr     solved.bmp
atbash.jpg      encrypted.txt  message.txt    rsacanbebroken.py  solved.png
b00tl3gRSA2.py  flag.png       message.txt.1  RSAEvenN.py
b00tl3gRSA3.py  leak           mindpsqs.py    scrambled1.png
basic-mod1.py   leak.tar       minirsa.py     scrambled2.png

┌──(dave㉿kaliv1rus)-[~/picoctf/crypto]
└─$ cd leak/                                                                     

┌──(dave㉿kaliv1rus)-[~/picoctf/crypto/leak]
└─$ ls                                                                           
passwords.txt  usernames.txt

┌──(dave㉿kaliv1rus)-[~/picoctf/crypto/leak]
└─$ grep -n "cultiris" usernames.txt                                             
378:cultiris

┌──(dave㉿kaliv1rus)-[~/picoctf/crypto/leak]
└─$ sed -n '378p' passwords.txt                                                  
cvpbPGS{P7e1S_54I35_71Z3}

```
https://gchq.github.io/CyberChef/#recipe=ROT13(true,true,false,13)&input=Y3ZwYlBHU3tQN2UxU181NEkzNV83MVozfQo
picoCTF{C7r1F_54V35_71M3}
#### Notas
#### Referencias
