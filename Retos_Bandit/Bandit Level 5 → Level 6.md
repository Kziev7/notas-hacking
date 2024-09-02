## Objetivo

The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:

- human-readable
- 1033 bytes in size
- not executable

## Datos de Acceso al Nivel

ssh bandit5@bandit.labs.overthewire.org -p 2220

## Solucion

```
bandit5@bandit:~$ ls
inhere
bandit5@bandit:~$ cd inhere
bandit5@bandit:~/inhere$ ls
maybehere00  maybehere03  maybehere06  maybehere09  maybehere12  maybehere15  maybehere18
maybehere01  maybehere04  maybehere07  maybehere10  maybehere13  maybehere16  maybehere19
maybehere02  maybehere05  maybehere08  maybehere11  maybehere14  maybehere17
bandit5@bandit:~/inhere$ ls -a
.            maybehere02  maybehere06  maybehere10  maybehere14  maybehere18
..           maybehere03  maybehere07  maybehere11  maybehere15  maybehere19
maybehere00  maybehere04  maybehere08  maybehere12  maybehere16
maybehere01  maybehere05  maybehere09  maybehere13  maybehere17
bandit5@bandit:~/inhere$ ls -l
total 80
drwxr-x--- 2 root bandit5 4096 Jul 17 15:57 maybehere00
drwxr-x--- 2 root bandit5 4096 Jul 17 15:57 maybehere01
drwxr-x--- 2 root bandit5 4096 Jul 17 15:57 maybehere02
drwxr-x--- 2 root bandit5 4096 Jul 17 15:57 maybehere03
drwxr-x--- 2 root bandit5 4096 Jul 17 15:57 maybehere04
drwxr-x--- 2 root bandit5 4096 Jul 17 15:57 maybehere05
drwxr-x--- 2 root bandit5 4096 Jul 17 15:57 maybehere06
drwxr-x--- 2 root bandit5 4096 Jul 17 15:57 maybehere07
drwxr-x--- 2 root bandit5 4096 Jul 17 15:57 maybehere08
drwxr-x--- 2 root bandit5 4096 Jul 17 15:57 maybehere09
drwxr-x--- 2 root bandit5 4096 Jul 17 15:57 maybehere10
drwxr-x--- 2 root bandit5 4096 Jul 17 15:57 maybehere11
drwxr-x--- 2 root bandit5 4096 Jul 17 15:57 maybehere12
drwxr-x--- 2 root bandit5 4096 Jul 17 15:57 maybehere13
drwxr-x--- 2 root bandit5 4096 Jul 17 15:57 maybehere14
drwxr-x--- 2 root bandit5 4096 Jul 17 15:57 maybehere15
drwxr-x--- 2 root bandit5 4096 Jul 17 15:57 maybehere16
drwxr-x--- 2 root bandit5 4096 Jul 17 15:57 maybehere17
drwxr-x--- 2 root bandit5 4096 Jul 17 15:57 maybehere18
drwxr-x--- 2 root bandit5 4096 Jul 17 15:57 maybehere19
bandit5@bandit:~/inhere$ cat maybehere00
cat: maybehere00: Is a directory
bandit5@bandit:~/inhere$ cd maybehere00
bandit5@bandit:~/inhere/maybehere00$ ls
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3
bandit5@bandit:~/inhere/maybehere00$ cd ..
bandit5@bandit:~/inhere$ find . -type f -size 1033c ! -executable
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
```

## Notas Adicionales

**`find . -type f -size 1033c ! -executable`** 
busca en el directorio actual (`.`) todos los archivos normales (`-type f`) que tienen un tamaño exacto de 1033 bytes (`-size 1033c`) y que no son ejecutables (`! -executable`).

## Referencias
