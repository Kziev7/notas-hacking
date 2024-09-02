## Objetivo

The password for the next level is stored in a file called **spaces in this filename** located in the home directory

## Datos de Acceso al Nivel

ssh bandit2@bandit.labs.overthewire.org -p 2220

## Solucion

```
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ ls -a
.  ..  .bash_logout  .bashrc  .profile  spaces in this filename
bandit2@bandit:~$ cat "spaces in this filename"
MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx

```


## Notas Adicionales

ls -a es para ver archivos ocultos aun que no era necesario

## Referencias

https://linuxhandbook.com/filename-spaces-linux/

