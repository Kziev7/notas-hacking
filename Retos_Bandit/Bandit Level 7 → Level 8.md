## Objetivo

The password for the next level is stored in the file **data.txt** next to the word **millionth**

## Datos de Acceso al Nivel

ssh bandit7@bandit.labs.overthewire.org -p 2220
## Solucion

```
bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ grep "millionth" data.txt
millionth       dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc
bandit7@bandit:~$ exit
```

## Notas Adicionales

Funciono el comando asi de sencillo porque estaba en la misma linea la contraseña y la palabra buscada.

## Referencias