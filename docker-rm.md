![](/assets/docker_rm.png)

\[root@localhost ~\]\# docker ps

CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES

\[root@localhost ~\]\# docker ps -n2

CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS                       PORTS               NAMES

153ea65bb543        centos              "/bin/bash"         18 minutes ago      Exited \(0\) 3 minutes ago                         adoring\_newton

ecf2a25b6f8c        centos              "/bin/bash"         20 minutes ago      Exited \(137\) 3 minutes ago                       mycentos0121

\[root@localhost ~\]\# docker rm ecf2a25b6f8c

ecf2a25b6f8c

\[root@localhost ~\]\# docker ps -n2

CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS                      PORTS               NAMES

153ea65bb543        centos              "/bin/bash"         18 minutes ago      Exited \(0\) 3 minutes ago                        adoring\_newton

3855c461790d        centos              "/bin/bash"         27 minutes ago      Exited \(0\) 22 minutes ago                       sleepy\_keldysh

\[root@localhost ~\]\#

