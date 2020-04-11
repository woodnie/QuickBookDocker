\[root@localhost ~\]\# docker ps

CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS               NAMES

06fb54229654        centos              "/bin/bash -c 'whileΓÇª"   5 minutes ago       Up 5 minutes                            dazzling\_vaughan

\[root@localhost ~\]\# docker top 06fb54229654

UID                 PID                 PPID                C                   STIME               TTY                 TIME

CMD

root                27831               27816               0                   22:58               ?                   00:00:00

/bin/bash -c while true; do echo hello world; sleep 2;done

root                28133               27831               0                   23:04               ?                   00:00:00

/usr/bin/coreutils --coreutils-prog-shebang=sleep /usr/bin/sleep 2

\[root@localhost ~\]\#

