## Descripción 
Reception of Special has been cool to say the least. That's why we made an exclusive version of Special, called Secure Comprehensive Interface for Affecting Linux Empirically Rad, or just 'Specialer'. With Specialer, we really tried to remove the distractions from using a shell. Yes, we took out spell checker because of everybody's complaining. But we think you will be excited about our new, reduced feature set for keeping you focused on what needs it the most. Please start an instance to test your very own copy of Specialer.`ssh -p 55341 ctf-player@saturn.picoctf.net`. The password is `3f39b042`
## Solución 
Nos conectamos al server y exploramos los archivos que contienen la bandera, este fue mi procedimiento
```
┌──(moonz㉿damoonz)-[~]
└─$ ssh -p 55341 ctf-player@saturn.picoctf.net
** WARNING: connection is not using a post-quantum key exchange algorithm.
** This session may be vulnerable to "store now, decrypt later" attacks.
** The server may need to be upgraded. See https://openssh.com/pq.html
ctf-player@saturn.picoctf.net's password: 
Specialer$ pwd
/home/ctf-player
Specialer$ cd 
.bash_history  .profile       ala/           
.hushlogin     abra/          sim/           
Specialer$ cd 
.bash_history  .profile       ala/           
.hushlogin     abra/          sim/           
Specialer$ for file in *
> do
>   if [ -d "$file" ]; then
>     echo "$file is a directory."
>   elif [ -f "$file" ]; then
>     echo "$file is a file."
>   fi
> done
abra is a directory.
ala is a directory.
sim is a directory.
Specialer$ cd abra
Specialer$ for file in *
> do
>   if [ -d "$file" ]; then
>     echo "$file is a directory."
>   elif [ -f "$file" ]; then
>     echo "$file is a file."
>   fi
> done
cadabra.txt is a file.
cadaniel.txt is a file.
Specialer$ cd .. 
Specialer$ cd ala
Specialer$ for file in *
> do
>   if [ -d "$file" ]; then
>     echo "$file is a directory."
>   elif [ -f "$file" ]; then
>     echo "$file is a file."
>   fi
> done
kazam.txt is a file.
mode.txt is a file.
Specialer$ cd ..
Specialer$ ls
-bash: ls: command not found
Specialer$ cd 
.bash_history  .profile       ala/           
.hushlogin     abra/          sim/           
Specialer$ cd sim/
Specialer$ for file in *
> do
>   if [ -d "$file" ]; then
>     echo "$file is a directory."
>   elif [ -f "$file" ]; then
>     echo "$file is a file."
>   fi
> done
city.txt is a file.
salabim.txt is a file.
Specialer$ for folder in abra ala sim
> do
>   cd "$folder"
>   for file in *
>   do
>     if [ -d "$file" ]; then
>       echo "$file: directory."
>     elif [ -f "$file" ]; then
>       echo "$folder/$file:"
>       printf "%s " $(<$file) # input redirection; alternative to 'cat'
>       printf "\n\n"
>     fi
>   done
>   cd ..
> done
-bash: cd: abra: No such file or directory
abra/city.txt:
05ed181c-4aa0-4d4a-8505-2fe6ca9097d3 

abra/salabim.txt:
#He was so kind, such a gentleman tied to the oceanside# 

ala/kazam.txt:
return 0 picoCTF{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_811ae7e9}
```
picoCTF{y0u_d0n7_4ppr3c1473_wh47_w3r3_d01ng_h3r3_811ae7e9}
## Notas
## Referencias