## Objetivo

The password for the next level is stored **somewhere on the server** and has all of the following properties:

- owned by user bandit7
- owned by group bandit6
- 33 bytes in size

## Datos de Acceso al Nivel

ssh bandit6@bandit.labs.overthewire.org -p 2220

## Solucion

```
bandit6@bandit:~$ ls
bandit6@bandit:~$ ls -u
bandit6@bandit:~$ ls -l
total 0
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
```

## Notas Adicionales

![[Pasted image 20240826191546.png]]

## Referencias

IA del buscador de Google