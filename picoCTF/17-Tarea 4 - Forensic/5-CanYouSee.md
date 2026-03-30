## CanYouSee

### Descripción
How about some hide and seek? Download this file [here](https://artifacts.picoctf.net/c_titan/131/unknown.zip).
### Solución
#### Solución 1
Este problema pensé que iba a ser como el de picoCTF/13- Forensic 3/3-Matryoshka doll, pero al final sólo era unzipear el zip y ver los metadatos de la imagen. Así fue como descubrí la flag:
```
┌──(dave㉿kaliv1rus)-[~/picoctf/forensic/CanYouSee]
└─$ binwalk unknown.zip 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             Zip archive data, at least v2.0 to extract, compressed size: 2252116, uncompressed size: 2263829, name: ukn_reality.jpg
2252274       0x225DF2        End of Zip archive, footer length: 22


┌──(dave㉿kaliv1rus)-[~/picoctf/forensic/CanYouSee]
└─$ xxd -l 20 unknown.zip 
00000000: 504b 0304 1400 0000 0800 bd00 6c58 31bc  PK..........lX1.
00000010: e704 545d                                ..T]

┌──(dave㉿kaliv1rus)-[~/picoctf/forensic/CanYouSee]
└─$ binwalk -e unknown.zip 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             Zip archive data, at least v2.0 to extract, compressed size: 2252116, uncompressed size: 2263829, name: ukn_reality.jpg

WARNING: One or more files failed to extract: either no utility was found or it's unimplemented


┌──(dave㉿kaliv1rus)-[~/picoctf/forensic/CanYouSee]
└─$ ls                                                                                                                                                                
unknown.zip  _unknown.zip.extracted

┌──(dave㉿kaliv1rus)-[~/picoctf/forensic/CanYouSee]
└─$ unzip unknown.zip 
Archive:  unknown.zip
  inflating: ukn_reality.jpg         

┌──(dave㉿kaliv1rus)-[~/picoctf/forensic/CanYouSee]
└─$ ls                                                                                                                                                                
ukn_reality.jpg  unknown.zip  _unknown.zip.extracted

┌──(dave㉿kaliv1rus)-[~/picoctf/forensic/CanYouSee]
└─$ open ukn_reality.jpg                                                                                                                                              

┌──(dave㉿kaliv1rus)-[~/picoctf/forensic/CanYouSee]
└─$ strings ukn_reality.jpg | grep pico

┌──(dave㉿kaliv1rus)-[~/picoctf/forensic/CanYouSee]
└─$ binwalk ukn_reality.jpg 

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             JPEG image data, JFIF standard 1.01


┌──(dave㉿kaliv1rus)-[~/picoctf/forensic/CanYouSee]
└─$ exiftool ukn_reality.jpg 
ExifTool Version Number         : 13.36
File Name                       : ukn_reality.jpg
Directory                       : .
File Size                       : 2.3 MB
File Modification Date/Time     : 2024:03:11 18:05:57-06:00
File Access Date/Time           : 2026:03:29 21:13:29-06:00
File Inode Change Date/Time     : 2026:03:29 21:13:09-06:00
File Permissions                : -rw-r--r--
File Type                       : JPEG
File Type Extension             : jpg
MIME Type                       : image/jpeg
JFIF Version                    : 1.01
Resolution Unit                 : inches
X Resolution                    : 72
Y Resolution                    : 72
XMP Toolkit                     : Image::ExifTool 11.88
Attribution URL                 : cGljb0NURntNRTc0RDQ3QV9ISUREM05fZDhjMzgxZmR9Cg==
Image Width                     : 4308
Image Height                    : 2875
Encoding Process                : Baseline DCT, Huffman coding
Bits Per Sample                 : 8
Color Components                : 3
Y Cb Cr Sub Sampling            : YCbCr4:2:0 (2 2)
Image Size                      : 4308x2875
Megapixels                      : 12.4

┌──(dave㉿kaliv1rus)-[~/picoctf/forensic/CanYouSee]
└─$ echo cGljb0NURntNRTc0RDQ3QV9ISUREM05fZDhjMzgxZmR9Cg== | base64 -d
picoCTF{ME74D47A_HIDD3N_d8c381fd}
```

picoCTF{ME74D47A_HIDD3N_d8c381fd}


### Notas adicionales

### Referencias

-