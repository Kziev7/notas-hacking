## Objetivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL/TLS encryption.

**Helpful note: Getting “DONE”, “RENEGOTIATING” or “KEYUPDATE”? Read the “CONNECTED COMMANDS” section in the manpage.**

## Datos de Acceso al Nivel

ssh bandit15@bandit.labs.overthewire.org -p 2220

## Solucion

```
bandit14@bandit:~$ openssl s_client -connect localhost:30001
CONNECTED(00000003)
Can't use SSL_get_servername
depth=0 CN = localhost
verify error:num=18:self-signed certificate
verify return:1
depth=0 CN = localhost
verify error:num=10:certificate has expired
notAfter=Feb 10 11:24:06 2023 GMT
verify return:1
depth=0 CN = localhost
notAfter=Feb 10 11:24:06 2023 GMT
verify return:1
---
Certificate chain
0 s:CN = localhost
i:CN = localhost
a:PKEY: rsaEncryption, 2048 (bit); sigalg: RSA-SHA1
v:NotBefore: Feb 10 11:23:06 2023 GMT; NotAfter: Feb 10 11:24:06
2023 GMT
---
Server certificate

...
...
...
---
read R BLOCK
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
Correct!
JQttfApK4SeyHwDlI9SXGR50qclOAil1
```

## Notas Adicionales
**Seguridad de la Capa de Transporte** (**TLS**) es a [protocolo criptográfico](https://en.wikipedia.org/wiki/Cryptographic_protocol "Protocolo criptográfico") diseñado para proporcionar seguridad de comunicaciones a través de una red informática.

## Referencias
[Secure Socket Layer/Transport Layer Security en Wikipedia](https://en.wikipedia.org/wiki/Transport_Layer_Security)

