## Objetivo

The password for the next level is stored in the file **data.txt**, which contains base64 encoded data

## Datos de Acceso al Nivel

ssh bandit10@bandit.labs.overthewire.org -p 2220

## Solucion

```
bandit10@bandit:~$ echo "hola mundo cruel" | base64
aG9sYSBtdW5kbyBjcnVlbAo=
bandit10@bandit:~$ echo aG9sYSBtdW5kbyBjcnVlbAo= | base64 -d
hola mundo cruel
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIGR0UjE3M2ZaS2IwUlJzREZTR3NnMlJXbnBOVmozcVJyCg==
bandit10@bandit:~$ echo "VGhlIHBhc3N3b3JkIGlzIGR0UjE3M2ZaS2IwUlJzREZTR3NnMlJXbnBOVmozcVJyCg==" | base64 -d
The password is dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
bandit10@bandit:~$ exit
```

## Notas Adicionales

base64 funciona para codificar el texto que nosotros queramos, a la vez, base64 -d nos ayuda a decodificar.
Tambien se puede usar cyberchef

## Referencias

El prof Carlos Castañeda