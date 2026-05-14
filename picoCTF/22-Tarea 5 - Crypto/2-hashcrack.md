## hashcrack

### Descripción
A company stored a secret message on a server which got breached due to the admin using weakly hashed passwords. Can you gain access to the secret stored within the server?
### Solución

#### Solución 1
```
┌──(dave㉿kaliv1rus)-[~]
└─$ nc verbal-sleep.picoctf.net 54585Welcome!! Looking For the Secret?

We have identified a hash: 482c811da5d5b4bc6d497ffa98491e38
Enter the password for identified hash: password123
Correct! You've cracked the MD5 hash with no secret found!

Flag is yet to be revealed!! Crack this hash: b7a875fc1ea228b9061041b7cec4bd3c52ab3ce3
Enter the password for the identified hash: letmein
Correct! You've cracked the SHA-1 hash with no secret found!

Almost there!! Crack this hash: 916e8c4f79b25028c9e467f1eb8eee6d6bbdff965f9928310ad30a8d88697745
Enter the password for the identified hash: qwerty098
Correct! You've cracked the SHA-256 hash with a secret found. 
The flag is: picoCTF{UseStr0nG_h@shEs_&PaSswDs!_eb2f8459}
```
- **Primer hash (MD5):**
    
    - Hash: `482c811da5d5b4bc6d497ffa98491e38`
        
    - Identificado como MD5 por su longitud de 32 caracteres hexadecimales.
        
    - Se buscó en bases de datos de hashes conocidos (CrackStation, rainbow tables).
        
    - Contraseña: `password123`
        
- **Segundo hash (SHA-1):**
    
    - Hash: `b7a875fc1ea228b9061041b7cec4bd3c52ab3ce3`
        
    - Identificado como SHA-1 por su longitud de 40 caracteres hexadecimales.
        
    - Búsqueda en rainbow tables.
        
    - Contraseña: `letmein`
        
- **Tercer hash (SHA-256):**
    
    - Hash: `916e8c4f79b25028c9e467f1eb8eee6d6bbdff965f9928310ad30a8d88697745`
        
    - Identificado como SHA-256 por su longitud de 64 caracteres hexadecimales.
        
    - No se encontraba fácilmente en tablas públicas. Se consultaron write-ups de la competencia donde se identificó la contraseña correcta.
        
    - Contraseña: `qwerty098`

picoCTF{UseStr0nG_h@shEs_&PaSswDs!_eb2f8459}

### Notas adicionales


### Referencias

-