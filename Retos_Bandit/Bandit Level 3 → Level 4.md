
## Objetivo

The password for the next level is stored in a hidden file in the **inhere** directory.

## Datos de Acceso al Nivel

ssh bandit3@bandit.labs.overthewire.org -p 2220
## Solucion
```
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere
bandit3@bandit:~/inhere$ ls
bandit3@bandit:~/inhere$ ls -a
.  ..  ...Hiding-From-You
bandit3@bandit:~/inhere$ cat ...Hiding-From-You
2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ
bandit3@bandit:~/inhere$
```

## Notas Adicionales

ls -a para archivos ocultos

## Referencias
