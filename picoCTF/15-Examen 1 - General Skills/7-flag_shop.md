## Descripción 
There's a flag shop selling stuff, can you buy a flag?[Source](https://challenge-files.picoctf.net/c_fickle_tempest/8ff1a012a01d1cbdaff34d98276201480b3a664509284c48bb108e0e01d3551d/store.c). Connect with nc fickle-tempest.picoctf.net 53659.
## Solución 
Nos conectamos y usamos el menú.
```
┌──(moonz㉿damoonz)-[~/Documentos/picoctf/fixme3/src]
└─$ nc fickle-tempest.picoctf.net 53659
Welcome to the flag exchange
We sell flags

1. Check Account Balance

2. Buy Flags

3. Exit

 Enter a menu selection
1



 Balance: 1100 


Welcome to the flag exchange
We sell flags

1. Check Account Balance

2. Buy Flags

3. Exit

 Enter a menu selection
2
Currently for sale
1. Defintely not the flag Flag
2. 1337 Flag
1
These knockoff Flags cost 900 each, enter desired quantity
3000000

The final cost is: -1594967296

Your current balance after transaction: 1594968396

Welcome to the flag exchange
We sell flags

1. Check Account Balance

2. Buy Flags

3. Exit

 Enter a menu selection
2
Currently for sale
1. Defintely not the flag Flag
2. 1337 Flag
2
1337 flags cost 100000 dollars, and we only have 1 in stock
Enter 1 to buy one1
YOUR FLAG IS: picoCTF{m0n3y_bag5_4E85dfe5}



```
picoCTF{m0n3y_bag5_4E85dfe5}
## Notas
## Referencias