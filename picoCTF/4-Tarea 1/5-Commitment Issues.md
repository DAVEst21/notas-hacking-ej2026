## Commitment Issues

### Descripción
I accidentally wrote the flag down. Good thing I deleted it!You download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_titan/138/challenge.zip)
### Solución

#### Solución 1
Obtenemos con wget el archivo zip, y posteriormente con unzip lo descomprimimos.
```
DAVEst-picoctf@webshell:~/drop-in$ git log
DAVEst-picoctf@webshell:~/drop-in$ git checkout b562f0b425907789d11d2fe2793e67592dc6be93
Note: switching to 'b562f0b425907789d11d2fe2793e67592dc6be93'.

You are in 'detached HEAD' state. You can look around, make experimental
changes and commit them, and you can discard any commits you make in this
state without impacting any branches by switching back to a branch.

If you want to create a new branch to retain commits you create, you may
do so (now or later) by using -c with the switch command. Example:

  git switch -c <new-branch-name>

Or undo this operation with:

  git switch -

Turn off this advice by setting config variable advice.detachedHead to false

HEAD is now at b562f0b create flag
DAVEst-picoctf@webshell:~/drop-in$ cat message.txt 
picoCTF{s@n1t1z3_c785c319}
```
picoCTF{s@n1t1z3_c785c319}
### Notas adicionales

### Referencias

-