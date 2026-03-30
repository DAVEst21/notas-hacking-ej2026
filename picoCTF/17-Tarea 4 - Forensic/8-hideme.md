## hideme

### Descripción
Every file gets a flag. The SOC analyst saw one image been sent back and forth between two people. They decided to investigate and found out that there was more than what meets the eye [here](https://artifacts.picoctf.net/c/258/flag.png).
### Solución

#### Solución 1
Este fue el recorrido que hice para obtener la bandera:
```
┌──(dave㉿kaliv1rus)-[~/picoctf/forensic/hideme]
└─$ xxd -l 20 flag.png 
00000000: 8950 4e47 0d0a 1a0a 0000 000d 4948 4452  .PNG........IHDR
00000010: 0000 0200                                ....

┌──(dave㉿kaliv1rus)-[~/picoctf/forensic/hideme]
└─$ binwalk flag.png 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             PNG image, 512 x 504, 8-bit/color RGBA, non-interlaced
41            0x29            Zlib compressed data, compressed
39739         0x9B3B          Zip archive data, at least v1.0 to extract, name: secret/
39804         0x9B7C          Zip archive data, at least v2.0 to extract, compressed size: 2876, uncompressed size: 3029, name: secret/flag.png
42915         0xA7A3          End of Zip archive, footer length: 22


┌──(dave㉿kaliv1rus)-[~/picoctf/forensic/hideme]
└─$ binwalk -e flag.png                                                                                                                                               

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
41            0x29            Zlib compressed data, compressed
39739         0x9B3B          Zip archive data, at least v1.0 to extract, name: secret/
39804         0x9B7C          Zip archive data, at least v2.0 to extract, compressed size: 2876, uncompressed size: 3029, name: secret/flag.png

WARNING: One or more files failed to extract: either no utility was found or it's unimplemented


┌──(dave㉿kaliv1rus)-[~/picoctf/forensic/hideme]
└─$ ls                                                                                                                                                                
flag.png  _flag.png.extracted

┌──(dave㉿kaliv1rus)-[~/picoctf/forensic/hideme]
└─$ cd _flag.png.extracted/                                                                                                                                           

┌──(dave㉿kaliv1rus)-[~/picoctf/forensic/hideme/_flag.png.extracted]
└─$ ls                                                                                                                                                                
29  29.zlib  9B3B.zip  secret

┌──(dave㉿kaliv1rus)-[~/picoctf/forensic/hideme/_flag.png.extracted]
└─$ cd secret/                                                                                                                                                        

┌──(dave㉿kaliv1rus)-[~/picoctf/forensic/hideme/_flag.png.extracted/secret]
└─$ ls                                                                                                                                                                
flag.png

┌──(dave㉿kaliv1rus)-[~/picoctf/forensic/hideme/_flag.png.extracted/secret]
└─$ open flag.png    
```
picoCTF{Hiddinng_An_Imag3_within_@n_ima9e_d55982e8}
### Notas adicionales


### Referencias

-