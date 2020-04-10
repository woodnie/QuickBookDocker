\[root@localhost ~\]\# docker ps

CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES

153ea65bb543        centos              "/bin/bash"         13 minutes ago      Up 3 seconds                            adoring\_newton

ecf2a25b6f8c        centos              "/bin/bash"         15 minutes ago      Up 5 minutes                            mycentos0121

\[root@localhost ~\]\# docker stop 153ea65bb543

153ea65bb543

\[root@localhost ~\]\# docker ps

CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES

ecf2a25b6f8c        centos              "/bin/bash"         17 minutes ago      Up 6 minutes                            mycentos0121

\[root@localhost ~\]\# docker kill ecf2a25b6f8c

ecf2a25b6f8c

\[root@localhost ~\]\# docker ps

CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES

\[root@localhost ~\]\#

