## repetitions

### Descripción
Can you make sense of this file?Download the file [here](https://artifacts.picoctf.net/c/475/enc_flag).
### Solución

#### Solución 1
```
DAVEst-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/475/enc_flag
--2026-02-11 15:02:29--  https://artifacts.picoctf.net/c/475/enc_flag
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.170.131.18, 3.170.131.33, 3.170.131.72, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.170.131.18|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 349 [application/octet-stream]
Saving to: 'enc_flag'

enc_flag               100%[==========================>]     349  --.-KB/s    in 0s      

2026-02-11 15:02:29 (4.41 MB/s) - 'enc_flag' saved [349/349]

DAVEst-picoctf@webshell:~$ ls
enc_flag
DAVEst-picoctf@webshell:~$ strings enc_flag 
VmpGU1EyRXlUWGxTYmxKVVYwZFNWbGxyV21GV1JteDBUbFpPYWxKdFVsaFpWVlUxWVZaS1ZWWnVh
RmRXZWtab1dWWmtSMk5yTlZWWApiVVpUVm10d1VWZFdVa2RpYlZaWFZtNVdVZ3BpU0VKeldWUkNk
MlZXVlhoWGJYQk9VbFJXU0ZkcVRuTldaM0JZVWpGS2VWWkdaSGRXCk1sWnpWV3hhVm1KRk5XOVVW
VkpEVGxaYVdFMVhSbFZrTTBKVVZXcE9VazFXV2toT1dHUllDbUY2UWpSWk1GWlhWa2RHZEdWRlZs
aGkKYlRrelZERldUMkpzUWxWTlJYTkxDZz09Cg==
```
picoCTF{base64_n3st3d_dic0d!n8_d0wnl04d3d_492767d2}

https://gchq.github.io/CyberChef/#recipe=From_Base64('A-Za-z0-9%2B/%3D',true,false)From_Base64('A-Za-z0-9%2B/%3D',true,false)From_Base64('A-Za-z0-9%2B/%3D',true,false)From_Base64('A-Za-z0-9%2B/%3D',true,false)From_Base64('A-Za-z0-9%2B/%3D',true,false)From_Base64('A-Za-z0-9%2B/%3D',true,false)&input=Vm1wR1UxRXlSWGxVV0d4VFlteEtWVll3WkZOV2JHeHlWMjFHVjFKdGVEQlViRnBQWVd4S2RGVnNhRnBXVmxVeFdWWmFTMVpXV25WaA0KUm1SWFpXdGFiMWRXV210U01rNXlUbFpXV0FwaVZWcFVWbTEwZDFWV1pGZFZhMlJwWWxaYVdGWnROVmRWWjNCcFUwVktlbGRXVWtOaw0KTWxaWFZsaG9XR0pZUWs5VmJGSlhVMFprY1ZSdVRsZGFNMEpaVldwR1MyVldXa2RhU0dSWENrMXNXbnBXVjNoaFZtMUtSazVYT1ZWVw0KVmtwRVZHeGFZVmRGTVZoU2JGWnJUVEJLVlZaWGNFOVZhekZYVjJ0b1QxZEhVbGxEYlVZMlVXcFNXazFHV2xoV2EyUkhaRWRXUmxacw0KYUdrS1lsUnJlbFpFUmxkVU1rcHpVV3hXVGxKWVRreERaejA5Q2c9PQ&ieol=CRLF
### Notas adicionales
### Referencias

-