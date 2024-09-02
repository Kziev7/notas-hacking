## Objetivo

The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work. Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv (read the manpages!)

## Datos de Acceso al Nivel

ssh bandit12@bandit.labs.overthewire.org -p 2220

## Solucion
```
bandit12@bandit:~$ ls
data.txt
bandit12@bandit:~$ xxd -r data.txt | file -
/dev/stdin: gzip compressed data, was "data2.bin", last modified: Wed Jul 17 15:57:06 2024, max compression, from Unix
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat
The password is FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
```

## Notas Adicionales

Ir descomprimiendo el archivo conforme te diga file - que tipo de archivo es



## Referencias

[Hex dump on Wikipedia](https://en.wikipedia.org/wiki/Hex_dump)


