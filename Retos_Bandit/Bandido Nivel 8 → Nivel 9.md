## Objetivo

The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once

## Datos de Acceso al Nivel

ssh bandit8@bandit.labs.overthewire.org -p 2220

## Solucion

```
bandit8@bandit:~$ ls
data.txt
bandit8@bandit:~$ sort data.txt | uniq -u
4CKMh1JI91bUIZZPXDqGanal4xvAg0JM
bandit8@bandit:~$ exit
```

## Notas Adicionales

el comando sort, que nos sirve para ordenar archivos, se utiliza en conjunto con el comando uniq -u que nos ayuda a filtrar lineas que no se repitan, es decir que sean unicas.

## Referencias
https://docs.rockylinux.org/es/books/admin_guide/04-advanced-commands/#:~:text=El%20comando%20uniq%20es%20un,de%20los%20registros%20eliminando%20duplicados.&text=uniq%20requiere%20que%20el%20archivo,porque%20solo%20compara%20l%C3%ADneas%20consecutivas.