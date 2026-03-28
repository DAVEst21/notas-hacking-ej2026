## Descripción 
If you want to hash with the best, beat this test!`nc saturn.picoctf.net 62498`
## Solución 
Solamente nos conectamos al puerto y se nos muestran preguntas para convertir cadenas a md5, usando cyberchef se hizo la conversión y se ingresa la respuesta hasta que sale la bandera
```
┌──(moonz㉿damoonz)-[~]
└─$ nc saturn.picoctf.net 62498
Please md5 hash the text between quotes, excluding the quotes: 'Clark Gable'
Answer: 
e4cfcc510ba955ce7e3458a9a88bb450
e4cfcc510ba955ce7e3458a9a88bb450
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'Chinatown'
Answer: 
09e49bb61f0323a3bfbe8937e2e031e8
09e49bb61f0323a3bfbe8937e2e031e8
Correct.
Please md5 hash the text between quotes, excluding the quotes: 'Abraham Lincoln'
Answer: 
2f7cfa603df2a25fce27ad69cd4be673
2f7cfa603df2a25fce27ad69cd4be673
Correct.
picoCTF{4ppl1c4710n_r3c31v3d_bf2ceb02}


```
picoCTF{4ppl1c4710n_r3c31v3d_bf2ceb02}
## Notas
## Referencias