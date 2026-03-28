## Descripción 
Python scripts are invoked kind of like programs in the Terminal...Can you run [ende.py](https://challenge-files.picoctf.net/c_wily_courier/1b9b921ec0fd3ea71d7e326c84ff94912e8e7d2d67c277af04005cace61cf230/ende.py) using [password.txt](https://challenge-files.picoctf.net/c_wily_courier/1b9b921ec0fd3ea71d7e326c84ff94912e8e7d2d67c277af04005cace61cf230/password.txt) to get [flag.txt.en](https://challenge-files.picoctf.net/c_wily_courier/1b9b921ec0fd3ea71d7e326c84ff94912e8e7d2d67c277af04005cace61cf230/flag.txt.en)?
## Solución 
Descargamos los 3 archivos, leemos el archivo que contiene la contraseña para usarla en este comando que desencripta la bandera.
```
┌──(moonz㉿damoonz)-[~/Documentos/picoctf]
└─$ python ende.py -d flag.txt.en
Please enter the password:720b6ad346f84cd483c60c7464dd95d4
picoCTF{4p0110_1n_7h3_h0us3_9c5f9bcf}
```
picoCTF{4p0110_1n_7h3_h0us3_9c5f9bcf}
## Notas
## Referencias
