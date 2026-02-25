## binhexa

### Descripción
How well can you perfom basic binary operations?

Additional details will be available after launching your challenge instance.
### Solución

#### Solución 1
```
DAVEst-picoctf@webshell:~$ nc titan.picoctf.net 64227

Welcome to the Binary Challenge!"
Your task is to perform the unique operations in the given order and find the final result in hexadecimal that yields the flag.

Binary Number 1: 01111110
Binary Number 2: 01101110


Question 1/6:
Operation 1: '|'
Perform the operation on Binary Number 1&2.
Enter the binary result: 0b1111110
Correct!

Question 2/6:
Operation 2: '>>'
Perform a right shift of Binary Number 2 by 1 bits .
Enter the binary result: 0
Incorrect. Try again
Enter the binary result: 0b0
Incorrect. Try again
Enter the binary result: 0b110111
Correct!

Question 3/6:
Operation 3: '+'
Perform the operation on Binary Number 1&2.
Enter the binary result: 0b11101100 
Correct!

Question 4/6:
Operation 4: '*'
Perform the operation on Binary Number 1&2.
Enter the binary result: 0b11011000100100 
Correct!

Question 5/6:
Operation 5: '&'
Perform the operation on Binary Number 1&2.
Enter the binary result: 0b1101110 
Correct!

Question 6/6:
Operation 6: '<<'
Perform a left shift of Binary Number 1 by 1 bits.
Enter the binary result: 0b11111100 
Correct!

Enter the results of the last operation in hexadecimal: 3131313131313030
Incorrect answer!

Enter the results of the last operation in hexadecimal: 0xfc

Correct answer!
The flag is: picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_675602ae}
```

en cmd con python:
```
Python 3.11.4 (tags/v3.11.4:d2340ef, Jun  7 2023, 05:45:37) [MSC v.1934 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>> a = bin(01111110)
  File "<stdin>", line 1
    a = bin(01111110)
            ^
SyntaxError: leading zeros in decimal integer literals are not permitted; use an 0o prefix for octal integers
>>> a = (011111101, 2)
  File "<stdin>", line 1
    a = (011111101, 2)
         ^
SyntaxError: leading zeros in decimal integer literals are not permitted; use an 0o prefix for octal integers
>>> a = int(011111101, 2)
  File "<stdin>", line 1
    a = int(011111101, 2)
            ^
SyntaxError: leading zeros in decimal integer literals are not permitted; use an 0o prefix for octal integers
>>> a = int('011111101', 2)
>>> a = int(01111110, 2)
  File "<stdin>", line 1
    a = int(01111110, 2)
            ^
SyntaxError: leading zeros in decimal integer literals are not permitted; use an 0o prefix for octal integers
>>> a = int('01111110', 2)
>>> b = int('01101110', 2)
>>> a | b
126
>>> bin (a | b)
'0b1111110'
>>> a >> b
0
>>> bin (a >> b)
'0b0'
>>> bin (b >> 1)
'0b110111'
>>> bin (a+b)
'0b11101100'
>>> bin (a*b)
'0b11011000100100'
>>> bin (a&b)
'0b1101110'
>>> bin (a<<1)
'0b11111100'
>>> hex (bin (a<<1))
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'str' object cannot be interpreted as an integer
>>> hex (bin (11111100))
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'str' object cannot be interpreted as an integer
>>> hex (bin ('11111100'))
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
TypeError: 'str' object cannot be interpreted as an integer
>>> hex (int ('11111100',2))
'0xfc'
```

picoCTF{b1tw^3se_0p3eR@tI0n_su33essFuL_675602ae}
### Notas adicionales

### Referencias

-