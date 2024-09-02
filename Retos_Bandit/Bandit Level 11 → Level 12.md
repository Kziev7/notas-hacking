## Objetivo

The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

## Datos de Acceso al Nivel

ssh bandit11@bandit.labs.overthewire.org -p 2220

## Solucion

```
bandit11@bandit:~$ ls -a
.  ..  .bash_logout  .bashrc  data.txt  .profile
bandit11@bandit:~$ file data.txt
data.txt: ASCII text
bandit11@bandit:~$ cat data.txt | tr [a-zA-Z] [n-za-mN-ZA-M]
The password is 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
```

## Notas Adicionales
rot13 es un sistema de cifrado en el que rota 13 posiciones en el alfabeto.

## Referencias

[Rot13 on Wikipedia](https://en.wikipedia.org/wiki/ROT13)
