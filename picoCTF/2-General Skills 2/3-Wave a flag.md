## Wave a flag

### Descripción
Can you invoke help flags for a tool or binary? This program has extraordinarily helpful information...[warm](https://challenge-files.picoctf.net/c_wily_courier/c293351e09ee53217c6a868e7f98a0a2ba0cf9cdc4e4ed0e18f685d47111c216/warm)
### Solución

#### Solución 1
```
DAVEst-picoctf@webshell:~$ wget https://challenge-files.picoctf.net/c_wily_courier/c293351e09ee53217c6a868e7f98a0a2ba0cf9cdc4e4ed0e18f685d47111c216/warm
--2026-02-11 14:16:54--  https://challenge-files.picoctf.net/c_wily_courier/c293351e09ee53217c6a868e7f98a0a2ba0cf9cdc4e4ed0e18f685d47111c216/warm
Resolving challenge-files.picoctf.net (challenge-files.picoctf.net)... 3.160.5.95, 3.160.5.64, 3.160.5.18, ...
Connecting to challenge-files.picoctf.net (challenge-files.picoctf.net)|3.160.5.95|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 19312 (19K) [application/octet-stream]
Saving to: 'warm'

warm                   100%[==========================>]  18.86K  --.-KB/s    in 0.01s   

2026-02-11 14:16:55 (1.88 MB/s) - 'warm' saved [19312/19312]

DAVEst-picoctf@webshell:~$ file warm
warm: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, BuildID[sha1]=9e46ec8729d2f2aa8ffc4b1cdc058081bddcfe67, for GNU/Linux 3.2.0, with debug_info, not stripped
DAVEst-picoctf@webshell:~$ chmod +x warm  
DAVEst-picoctf@webshell:~$ ./warm 
Hello user! Pass me a -h to learn what I can do!
DAVEst-picoctf@webshell:~$ ./warm -h
Oh, help? I actually don't do much, but I do have this flag here: picoCTF{b1scu1ts_4nd_gr4vy_ac5832c}
```
picoCTF{b1scu1ts_4nd_gr4vy_ac5832c}
### Notas adicionales
- Este problema nos recuerda que los ejecutables tienen comandos como -h.
### Referencias

-