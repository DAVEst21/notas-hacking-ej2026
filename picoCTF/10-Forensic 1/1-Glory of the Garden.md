## Glory of the Garden

### Descripción
This file contains more than it seems. Get the flag from [garden.jpg](https://challenge-files.picoctf.net/c_fickle_tempest/26ad1e959e2e6f15113d4dc2b43649625499d960e546d1b874357c6fcb8c5229/garden.jpg).
### Solución

#### Solución 1
Se pude ver la imagen en hexeditor y con ctrl + w se puede buscar la palabra pico y nos arroja lo siguiente
He
00230560  72 65 20 69  73 20 61 20   66 6C 61 67  3A 20 70 69                                                                                          re is a flag: pi
00230570  63 6F 43 54  46 7B 6D 6F   72 65 5F 74  68 61 6E 5F                                                                                          coCTF{more_than_
00230580  6D 33 33 74  73 5F 74 68   65 5F 33 79  33 33 33 66                                                                                          m33ts_the_3y333f
00230590  38 34 64 37  63 7D 0A                                                                                                                        84d7c}

picoCTF{more_than_m33ts_the_3y333f84d7c}

#### Solución 2
Con strings garden.jpg | grep pico nos arroja la bandera.

picoCTF{more_than_m33ts_the_3y333f84d7c}





### Notas adicionales
La informática forense es una rama de las ciencias digitales encargada de identificar, preservar, analizar y presentar evidencia electrónica de manera que sea admisible en procesos judiciales. Se utiliza para investigar ciberdelitos como fraude, robo de datos o intrusiones, garantizando una cadena de custodia sólida.

Un editor hexadecimal es un tipo de programa informático que permite a un usuario modificar archivos binarios. Los editores hexadecimales fueron diseñados para editar sectores de datos de disquetes o discos duros por lo que a veces se llaman "editores de sectores".

### Referencias

-