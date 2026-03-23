## WebNet1

### Descripción
We found this [packet capture](https://challenge-files.picoctf.net/c_fickle_tempest/d1e9add4e31989553f239ebf71ba5972f9bed7bd4932f931e14bfba80d75f815/capture.pcap) and [key](https://challenge-files.picoctf.net/c_fickle_tempest/d1e9add4e31989553f239ebf71ba5972f9bed7bd4932f931e14bfba80d75f815/picopico.key). Recover the flag.
### Solución

#### Solución 1 y 2
```
┌──(dave㉿kaliv1rus)-[~/picoctf/forensic/someta]                                                                                                                       
└─$ exiftool pico_img.png
ExifTool Version Number         : 13.36                                                                                                                                
File Name                       : pico_img.png                                                                                                                         
Directory                       : .                                                                                                                                    
File Size                       : 109 kB                                                                                                                               
File Modification Date/Time     : 2025:11:21 13:11:00-06:00                                                                                                            
File Access Date/Time           : 2026:03:09 08:17:22-06:00                                                                                                            
File Inode Change Date/Time     : 2026:03:09 08:17:22-06:00                                                                                                            
File Permissions                : -rw-rw-r--                                                                                                                           
File Type                       : PNG                                                                                                                                  
File Type Extension             : png
MIME Type                       : image/png
Image Width                     : 600
Image Height                    : 600
Bit Depth                       : 8
Color Type                      : RGB
Compression                     : Deflate/Inflate
Filter                          : Adaptive
Interlace                       : Noninterlaced
Software                        : Adobe ImageReady
XMP Toolkit                     : Adobe XMP Core 5.3-c011 66.145661, 2012/02/06-14:56:27
Creator Tool                    : Adobe Photoshop CS6 (Windows)
Instance ID                     : xmp.iid:A5566E73B2B811E8BC7F9A4303DF1F9B
Document ID                     : xmp.did:A5566E74B2B811E8BC7F9A4303DF1F9B
Derived From Instance ID        : xmp.iid:A5566E71B2B811E8BC7F9A4303DF1F9B
Derived From Document ID        : xmp.did:A5566E72B2B811E8BC7F9A4303DF1F9B
Artist                          : picoCTF{s0_m3ta_19ebefe2}
Image Size                      : 600x600
Megapixels                      : 0.360

┌──(dave㉿kaliv1rus)-[~/picoctf/forensic/someta]
└─$ exiftool pico_img.png -Artist                                                                                                                                      
Artist                          : picoCTF{s0_m3ta_19ebefe2}

┌──(dave㉿kaliv1rus)-[~/picoctf/forensic/someta]
└─$ strings pico_img.png | grep pico
picoCTF{s0_m3ta_19ebefe2}

```

### Notas adicionales
Los metadatos son "datos sobre los datos", información estructurada que describe, localiza, gestiona o ayuda a comprender recursos digitales (documentos, imágenes, correos). Incluyen atributos como autor, fecha, tamaño, formato y ubicación, siendo cruciales para la búsqueda, organización, preservación y seguridad de la información.
ExifTool permite ver los metadatos de cualquier archivo
### Referencias

-