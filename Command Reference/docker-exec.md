



\[root@localhost ~\]\# docker exec --help



Usage:  docker exec \[OPTIONS\] CONTAINER COMMAND \[ARG...\]



Run a command in a running container



Options:

  -d, --detach               Detached mode: run command in the background

      --detach-keys string   Override the key sequence for detaching a container

  -e, --env list             Set environment variables

  -i, --interactive          Keep STDIN open even if not attached

      --privileged           Give extended privileges to the command

  -t, --tty                  Allocate a pseudo-TTY

  -u, --user string          Username or UID \(format: &lt;name\|uid&gt;\[:&lt;group\|gid&gt;\]\)

  -w, --workdir string       Working directory inside the container

\[root@localhost ~\]\#



![](/assets/docker_exec.png)



\[root@localhost ~\]\# docker run -it centos

\[root@34cf6899e4c7 /\]\#

\[root@34cf6899e4c7 /\]\# \[root@localhost ~\]\#

\[root@localhost ~\]\# docker ps

CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES

34cf6899e4c7        centos              "/bin/bash"         3 minutes ago       Up 3 minutes                            nostalgic\_perlman



\[root@localhost ~\]\# docker exec -it 34cf6899e4c7 ls -l /tmp

total 8

-rwx------. 1 root root  671 Jan 13 21:49 ks-script-\_srt3u3c

-rwx------. 1 root root 1379 Jan 13 21:49 ks-script-gpqu\_kuo

\[root@localhost ~\]\# docker exec -it 34cf6899e4c7 /bin/bash

\[root@34cf6899e4c7 /\]\# ls -l /tmp

total 8

-rwx------. 1 root root  671 Jan 13 21:49 ks-script-\_srt3u3c

-rwx------. 1 root root 1379 Jan 13 21:49 ks-script-gpqu\_kuo

\[root@34cf6899e4c7 /\]\#



\[root@34cf6899e4c7 /\]\# read escape sequence

\[root@localhost ~\]\#

\[root@localhost ~\]\# docker attach 34cf6899e4c7

\[root@34cf6899e4c7 /\]\#

