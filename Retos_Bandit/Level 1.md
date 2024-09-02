## Objetivo

The password for the next level is stored in a file called **readme** located in the home directory. Use this password to log into bandit1 using SSH. Whenever you find a password for a level, use SSH (on port 2220) to log into that level and continue the game.

## Datos de Acceso al Nivel

ssh bandit1@bandit.labs.overthewire.org -p 2220


## Solucion

```
bandit1@bandit:~$ cat ./-
263JGJPfgU6LtdEvgfWU1XP5yac29mFx
```

## Notas Adicionales

En el comando `cat ./-`, el `./` se utiliza para indicar que el archivo que estás tratando de leer (`-`) se encuentra en el directorio actual.

ls, cd, cat, file, du, find

## Referencias
overthewire.org

