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
-----BEGIN CERTIFICATE-----
MIIDCzCCAfOgAwIBAgIEJiAX8TANBgkqhkiG9w0BAQUFADAUMRIwEAYDVQQDDAls
b2NhbGhvc3QwHhcNMjMwMjEwMTEyMzA2WhcNMjMwMjEwMTEyNDA2WjAUMRIwEAYD

VQQDDAlsb2NhbGhvc3QwggEiMA0GCSqGSIb3DQEBAQUAA4IBDwAwggEKAoIBAQC0
C9o3EhuCUFaRpKMx78H1Je9LrJGHF1RUV4u+rZFgcTv+RcNJA9G5ks3jgHkYMvnT
3Z3Vq0yeGf5SMBzZvGD6awxBV+r4iqII4zfaeJXSp2jS3VKtcZa6EF0I64CBq/4l
gK9GT/9guekqSER+fpN/cyOihCF34ovC5S3lI9hs6L/UdtMq1FC4UZ1SjZkFSb0F
znZfAqCQymFIwOzuDuBCTnweo1EOdDF5rHlQVJK0OmJo68qswBUiAa0lQNxcjbMZ
w3xicmFYfFBgVkxaLHstsz8vL7hdTWjtKNFJZcXCezGwDPYUe13M3N6uHdBWITpA
Q2+7n42ihPusFJmr54XPAgMBAAGjZTBjMBQGA1UdEQQNMAuCCWxvY2FsaG9zdDBL
BglghkgBhvhCAQ0EPhY8QXV0b21hdGljYWxseSBnZW5lcmF0ZWQgYnkgTmNhdC4g
U2VlIGh0dHBzOi8vbm1hcC5vcmcvbmNhdC8uMA0GCSqGSIb3DQEBBQUAA4IBAQBg
EoypqYh/MhVd4w4hM1+8LilU8WPRYNSmbuEjJ5dGhwJVBXfcFGBRUnT6+pVRj9Zs
4ejoQP0E3BwCglapumGvgRWO5YBxXPPqaaaeFUcSCfulfX9i69cG/9A1G2Wn25zf
aRI7Qwv8RCBVU8NZf8CV8WRu6EjqpegQA42u0O2nXh3LucUgJNk3OK7XymmPqeYe
z8eqagd4Rp9qtQ86Yg7zLr8NBup6+euaJhI2W323IrmBbDuPmU/aPUa1TaZubwKH
sU/iSDq5CA+ljy+6Dlb9mBT3DyotbkKsoBPGEgFl9E/VSUi/vQxRZ24MAU6aPAUT
SXZMfyeR5ADKNhvqxdS6
-----END CERTIFICATE-----
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

