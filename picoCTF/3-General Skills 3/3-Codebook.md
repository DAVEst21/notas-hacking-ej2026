## Codebook

### Descripción
Run the Python script `code.py` in the same directory as `codebook.txt`.

- [Download code.py](https://artifacts.picoctf.net/c/2/code.py)
- [Download codebook.txt](https://artifacts.picoctf.net/c/2/codebook.txt)
### Solución

#### Solución 1
```
DAVEst-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/2/codebook.txt
--2026-02-16 01:49:17--  https://artifacts.picoctf.net/c/2/codebook.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.92, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 27 [application/octet-stream]
Saving to: 'codebook.txt'

codebook.txt           100%[==========================>]      27  --.-KB/s    in 0s      

2026-02-16 01:49:17 (13.5 MB/s) - 'codebook.txt' saved [27/27]

DAVEst-picoctf@webshell:~$ ls
codebook.txt
DAVEst-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/2/code.py
--2026-02-16 01:49:37--  https://artifacts.picoctf.net/c/2/code.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.160.22.16, 3.160.22.92, 3.160.22.128, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.160.22.16|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1278 (1.2K) [application/octet-stream]
Saving to: 'code.py'

code.py                100%[==========================>]   1.25K  --.-KB/s    in 0s      

2026-02-16 01:49:37 (988 MB/s) - 'code.py' saved [1278/1278]

DAVEst-picoctf@webshell:~$ cat codebook.txt 
azbycxdwevfugthsirjqkplomn
DAVEst-picoctf@webshell:~$ cat code.py 

import random
import sys



def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_c) in zip(secret,new_key)])


flag_enc = chr(0x13) + chr(0x01) + chr(0x17) + chr(0x07) + chr(0x2c) + chr(0x3a) + chr(0x2f) + chr(0x1a) + chr(0x0d) + chr(0x53) + chr(0x0c) + chr(0x47) + chr(0x0a) + chr(0x5f) + chr(0x5e) + chr(0x02) + chr(0x3e) + chr(0x5a) + chr(0x56) + chr(0x5d) + chr(0x45) + chr(0x5d) + chr(0x58) + chr(0x31) + chr(0x5e) + chr(0x05) + chr(0x5f) + chr(0x53) + chr(0x5a) + chr(0x10) + chr(0x5f) + chr(0x0e) + chr(0x13)



def print_flag():
  try:
    codebook = open('codebook.txt', 'r').read()
    
    password = codebook[4] + codebook[14] + codebook[13] + codebook[14] +\
               codebook[23]+ codebook[25] + codebook[16] + codebook[0]  +\
               codebook[25]
               
    flag = str_xor(flag_enc, password)
    print(flag)
  except FileNotFoundError:
    print('Couldn\'t find codebook.txt. Did you download that file into the same directory as this script?')



def main():
  print_flag()



if __name__ == "__main__":
  main()

DAVEst-picoctf@webshell:~$ python code.py 
picoCTF{c0d3b00k_455157_7d102d7a}
```

picoCTF{c0d3b00k_455157_7d102d7a}
### Notas adicionales

### Referencias

-