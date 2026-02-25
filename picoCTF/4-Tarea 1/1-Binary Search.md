## Binary Search

### Descripción
Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!
### Solución

#### Solución 1
```
DAVEst-picoctf@webshell:~$ ssh -p 55745 ctf-player@atlas.picoctf.net
ctf-player@atlas.picoctf.net's password: 
Welcome to the Binary Search Game!
I'm thinking of a number between 1 and 1000.
Enter your guess: 500
Higher! Try again.
Enter your guess: 750
Lower! Try again.
Enter your guess: 625
Higher! Try again.
Enter your guess: 687
Higher! Try again.
Enter your guess: 718
Lower! Try again.
Enter your guess: 702
Lower! Try again.
Enter your guess: 694
Congratulations! You guessed the correct number: 694
Here's your flag: picoCTF{g00d_gu355_6dcfb67c}
Connection to atlas.picoctf.net closed.
```
Realizas manualmente búsqueda binaria.

picoCTF{g00d_gu355_6dcfb67c}
### Notas adicionales

### Referencias

-