## Objetivo

The password for the next level is stored in **/etc/bandit_pass/bandit14 and can only be read by user bandit14**. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. **Note:** **localhost** is a hostname that refers to the machine you are working on

## Datos de Acceso al Nivel

ssh bandit13@bandit.labs.overthewire.org -p 2220

## Solucion

```
bandit13@bandit:~$ ls
sshkey.private

bandit13@bandit:~$ ls -la
total 24
drwxr-xr-x  2 root     root     4096 Jul 17 15:57 .
drwxr-xr-x 70 root     root     4096 Jul 17 15:58 ..
-rw-r--r--  1 root     root      220 Mar 31 08:41 .bash_logout
-rw-r--r--  1 root     root     3771 Mar 31 08:41 .bashrc
-rw-r--r--  1 root     root      807 Mar 31 08:41 .profile
-rw-r-----  1 bandit14 bandit13 1679 Jul 17 15:57 sshkey.private
bandit13@bandit:~$ ssh -i sshkey.private bandit14@localhost -p 2220

This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Could not create directory '/home/bandit13/.ssh' (Permission denied).
Failed to add the host to the list of known hosts (/home/bandit13/.ssh/known_hosts).

bandit14@bandit:~$ whoami
bandit14
bandit14@bandit:~$ pwd
/home/bandit14
bandit14@bandit:~$ cat /etc/bandit_pass/bandit14
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS


```

## Notas Adicionales

Inicialmente ingresamos a bandit13 y ahi dentro vimos las llaves de bandit14 por lo que accedimos, despues solicitamos la contraseña de bandit14.

ssh-private-key - Una llave privada permite al usuario ingresar al al servidor ssh sin usar el password

para pasarle la llave privada se usa -i 
ssh -i sshkey.private bandit14@localhost -p 2220

## Referencias

[SSH/OpenSSH/Keys](https://help.ubuntu.com/community/SSH/OpenSSH/Keys)
