## Lets Warm Up
### Descripción
If I told you a word started with 0x70 in hexadecimal, what would it start with in ASCII?

### Solución
#### Solución 1
- Usando cyberchef
- https://gchq.github.io/CyberChef/#recipe=From_Hex('0x')&input=MHg3MA
#### Solución 2
- Usando Python
```
>>> int(0x70)
112
>>> chr(112)
'p'
```
### Notas adicionales
- Puede usarse incluso el intérprete de Python para convertir de hex a ascii
### Referencias
- https://gchq.github.io/CyberChef/#recipe=From_Hex('0x')&input=MHg3MA