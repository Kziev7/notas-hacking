## Objetivo

The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.

## Datos de Acceso al Nivel

ssh bandit9@bandit.labs.overthewire.org -p 2220

## Solucion

```
bandit9@bandit:~$ ls
data.txt
bandit9@bandit:~$ strings data.txt | grep "===="
\a!;========== the
========== passwordf
========== isc
========== FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
bandit9@bandit:~$ exit
```
## Notas Adicionales

El _comando_ “_strings_” es una herramienta muy útil en _Linux_ que permite extraer cadenas de texto legibles de archivos binarios.
La contraseña salio con eso pero decidi filtrarla aun mas con el grep


## Referencias

https://infolinux.es/comando-strings-de-linux-obten-cadenas-de-texto-de-archivos-article-about-linux-command-strings-retrieve-text-strings-from-files/

