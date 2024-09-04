
## Objetivo
The credentials for the next level can be retrieved by submitting the password of the current level to **a port on localhost in the range 31000 to 32000**. First find out which of these ports have a server listening on them. Then find out which of those speak SSL/TLS and which don’t. There is only 1 server that will give the next credentials, the others will simply send back to you whatever you send to it.

**Helpful note: Getting “DONE”, “RENEGOTIATING” or “KEYUPDATE”? Read the “CONNECTED COMMANDS” section in the manpage.**

## Datos de Acceso al Nivel

ssh bandit16@bandit.labs.overthewire.org -p 2220

## Solucion
```

bandit17@bandit.labs.overthewire.org -p2220

bandit17@bandit:~$ cat /etc/bandit_pass/bandit17
VwOSWtCA7lRKkTfbr2IDh6awj9RNZM5e
bandit17@bandit:~$ exit
```
## Notas Adicionales
A **escáner de puerto** es una aplicación diseñada para sondear un [servidor](https://en.wikipedia.org/wiki/Server_(computing) "Servidor (computación)") o [anfitrión](https://en.wikipedia.org/wiki/Host_(network) "Host (red)") para abrir [puertos](https://en.wikipedia.org/wiki/TCP_and_UDP_port "puerto TCP y UDP"). Tal aplicación puede ser utilizada por [administradores](https://en.wikipedia.org/wiki/Network_administrator "Administrador de red") para verificar [seguridad](https://en.wikipedia.org/wiki/Security "Seguridad") políticas de sus [redes](https://en.wikipedia.org/wiki/Computer_network "Red informática") y por [atacantes](https://en.wikipedia.org/wiki/Security_cracking "Seguridad craqueo") identificar [servicios de red](https://en.wikipedia.org/wiki/Network_service "Servicio de red") ejecutar en un host y explotar vulnerabilidades.

A **escaneo de puertos** o **portscan** es un proceso que envía solicitudes de clientes a una variedad de direcciones de puertos de servidor en un host, con el objetivo de encontrar un puerto activo; este no es un proceso nefasto en sí mismo. La mayoría de los usos de un escaneo de puertos no son ataques, sino sondas simples para determinar los servicios disponibles en una máquina remota.
## Referencias
[Escáner de puerto en Wikipedia](https://en.wikipedia.org/wiki/Port_scanner)