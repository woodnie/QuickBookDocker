\[root@localhost ~\]\# docker ps

CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES

153ea65bb543        centos              "/bin/bash"         11 seconds ago      Up 10 seconds                           adoring\_newton

![](/assets/docker_ps.png)



\[root@localhost ~\]\# docker ps -a

CONTAINER ID        IMAGE               COMMAND             CREATED              STATUS                      PORTS               NAMES

153ea65bb543        centos              "/bin/bash"         About a minute ago   Up About a minute                               adoring\_newton

ecf2a25b6f8c        centos              "/bin/bash"         4 minutes ago        Exited \(0\) 2 minutes ago                        mycentos0121

3855c461790d        centos              "/bin/bash"         10 minutes ago       Exited \(0\) 5 minutes ago                        sleepy\_keldysh

36fa12e581a2        centos              "/bin/bash"         13 minutes ago       Exited \(0\) 13 minutes ago                       musing\_shamir

f69f010a0b5c        hello-world         "/hello"            5 days ago           Exited \(0\) 5 days ago                           flamboyant\_hermann

5273397e8bd4        hello-world         "/hello"            7 days ago           Exited \(0\) 7 days ago                           flamboyant\_diffie

4e341be46adb        hello-world         "/hello"            7 days ago           Exited \(0\) 7 days ago                           intelligent\_perlman



\[root@localhost ~\]\# docker ps -l

CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES

153ea65bb543        centos              "/bin/bash"         2 minutes ago       Up 2 minutes                            adoring\_newton



\[root@localhost ~\]\# docker ps -aq

153ea65bb543

ecf2a25b6f8c

3855c461790d

36fa12e581a2

f69f010a0b5c

5273397e8bd4

4e341be46adb



\[root@localhost ~\]\# docker ps -lq

153ea65bb543

\[root@localhost ~\]\#



