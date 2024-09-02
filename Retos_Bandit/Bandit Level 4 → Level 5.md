
## Objetivo

The password for the next level is stored in the only human-readable file in the **inhere** directory. Tip: if your terminal is messed up, try the “reset” command.

## Datos de Acceso al Nivel

ssh bandit4@bandit.labs.overthewire.org -p 2220

## Solucion

```
bandit4@bandit:~/inhere$ ls
-file00  -file01  -file02  -file03  -file04  -file05  -file06  -file07  -file08  -file09
bandit4@bandit:~/inhere$ cat ./-file00
��,��␦����Yq��f�L���j␦�0����x�4Fbandit4@bandit:~/inhere$ cat ./-file01
N�.��bandit4@bandit:~/inhere$ cat ./-file02
��9������F��p������tk���%��bandit4@bandit:~/inhere$ cat ./-file03
�����n�Qy�y͍�{+R�bZ�k�F�*       bandit4@bandit:~/inhere$ cat ./-file04

l�����]�a߯-@gQ�÷�wz�P�ߠy�bandit4@bandit:~/inhere$ cat ./-file05
�pӻT9�F��3ˤ����)
T�՜F�ǭ�bandit4@bandit:~/inhere$ cat ./-file06
�QĹ�M���p4�-�8��=��!#g���bandit4@bandit:~/inhere$ cat ./-file07
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
bandit4@bandit:~/inhere$
```

## Notas Adicionales

Se hizo uso de ./ para poder leer el archivo

## Referencias