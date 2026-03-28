## Descripción 
Play this short game to get familiar with terminal applications and some of the most important rules in scope for picoCTF.Connect to the program with netcat:`$ nc verbal-sleep.picoctf.net 61757`
## Solución 
Al conectarnos al puerto entramos en un pequeño juego de preguntas y diálogos. Solo es necesario contestar un par de preguntas correctamente, para continuar solo es seguir dando enter.
Opción C (porque usar varias cuentas o cuentas compartidas puede descalificarnos):

```
Nyx brings up the registration page.

Options:
A) *Register multiple accounts*
B) *Share an account with a friend*
C) *Register a single, private account*
[a/b/c] > c
```
Opción A (jugar para conseguir la bandera):

```
"Oh interesting," Eibhilin says, "It seems like the sanity challenge is an old
school interactive fiction game."

---
(Press Enter to continue...)
---

Options:
A) *Play the game*
B) *Search the Ether for the flag*
[a/b] > a

```
 
 picoCTF{m1113n1um_3d1710n_8d7ec7f5}
## Notas
## Referencias