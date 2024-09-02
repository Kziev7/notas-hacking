## Objetivo

The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.

## Datos de Acceso al Nivel

ssh bandit14@bandit.labs.overthewire.org -p 2220


## Solucion

```
bandit14@bandit:~$ nc localhost 30000
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
Correct!
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo
```

## Notas Adicionales

nc - es una herramienta que permite conectarse 

## Referencias
