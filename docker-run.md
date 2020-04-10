\[root@localhost ~\]\# docker run --help



Usage:  docker run \[OPTIONS\] IMAGE \[COMMAND\] \[ARG...\]



![](/assets/docker_run.png)







\[root@localhost ~\]\# docker images centos

REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE

centos              latest              470671670cac        3 days ago          237MB

\[root@localhost ~\]\# docker run -it centos

\[root@153ea65bb543 /\]\#

\[root@localhost ~\]\# docker ps

CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES

153ea65bb543        centos              "/bin/bash"         11 seconds ago      Up 10 seconds                           adoring\_newton

\[root@localhost ~\]\#



\[root@localhost ~\]\# docker images centos

REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE

centos              latest              470671670cac        3 days ago          237MB

\[root@localhost ~\]\# docker run -it --name mycentos0121 centos

\[root@ecf2a25b6f8c /\]\#

\[root@localhost ~\]\# docker ps

CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES

ecf2a25b6f8c        centos              "/bin/bash"         9 seconds ago       Up 8 seconds                            mycentos0121

\[root@localhost ~\]\#



前台交互式启动 option -it:







后台启动option -d :



\[root@localhost ~\]\# docker run -d centos

ff93b8290d83b7d0ebba6663cc4d8b3c7345dfe7bfeb690bdb56cf3a25601fd9

\[root@localhost ~\]\# docker ps

CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES

\[root@localhost ~\]\#







