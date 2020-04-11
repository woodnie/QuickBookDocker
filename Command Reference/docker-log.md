

![](/assets/docker_log.png)

\[root@localhost ~\]\# docker run -d centos  /bin/bash -c  "while true; do echo hello world; sleep 2;done"

06fb542296547bc72d096e71d16e88caac6e1b1f7899f2e3617d7f481bd0bd2f

\[root@localhost ~\]\# docker ps

CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS               NAMES

06fb54229654        centos              "/bin/bash -c 'whileΓÇª"   3 seconds ago       Up 3 seconds                            dazzling\_vaughan

\[root@localhost ~\]\# docker log 06fb54229654

docker: 'log' is not a docker command.

See 'docker --help'

\[root@localhost ~\]\# docker logs 06fb54229654

hello world

hello world

hello world

hello world

hello world

hello world

hello world

hello world

hello world

hello world

hello world

hello world

hello world

hello world

hello world

hello world

hello world

\[root@localhost ~\]\# docker logs -t 06fb54229654

2020-01-21T14:58:46.555442309Z hello world

2020-01-21T14:58:48.557512652Z hello world

2020-01-21T14:58:50.559278864Z hello world

2020-01-21T14:58:52.561739014Z hello world

2020-01-21T14:58:54.563731771Z hello world

2020-01-21T14:58:56.565479745Z hello world

2020-01-21T14:58:58.567460773Z hello world

2020-01-21T14:59:00.569249930Z hello world

2020-01-21T14:59:02.571250516Z hello world

2020-01-21T14:59:04.573051151Z hello world

2020-01-21T14:59:06.575449667Z hello world

2020-01-21T14:59:08.577234551Z hello world

2020-01-21T14:59:10.579473696Z hello world

2020-01-21T14:59:12.581605470Z hello world

2020-01-21T14:59:14.583347989Z hello world

2020-01-21T14:59:16.585383550Z hello world

2020-01-21T14:59:18.587162333Z hello world

2020-01-21T14:59:20.589211886Z hello world

2020-01-21T14:59:22.590984922Z hello world

2020-01-21T14:59:24.593126392Z hello world

2020-01-21T14:59:26.594956286Z hello world

2020-01-21T14:59:28.596946331Z hello world

2020-01-21T14:59:30.598956860Z hello world

2020-01-21T14:59:32.600943786Z hello world

2020-01-21T14:59:34.602621904Z hello world

2020-01-21T14:59:36.604524151Z hello world

2020-01-21T14:59:38.606559608Z hello world

\[root@localhost ~\]\# docker logs -t -f 06fb54229654

2020-01-21T14:58:46.555442309Z hello world

2020-01-21T14:58:48.557512652Z hello world

2020-01-21T14:58:50.559278864Z hello world

2020-01-21T14:58:52.561739014Z hello world

2020-01-21T14:58:54.563731771Z hello world

2020-01-21T14:58:56.565479745Z hello world

2020-01-21T14:58:58.567460773Z hello world

2020-01-21T14:59:00.569249930Z hello world

2020-01-21T14:59:02.571250516Z hello world

2020-01-21T14:59:04.573051151Z hello world

2020-01-21T14:59:06.575449667Z hello world

2020-01-21T14:59:08.577234551Z hello world

2020-01-21T14:59:10.579473696Z hello world

2020-01-21T14:59:12.581605470Z hello world

2020-01-21T14:59:14.583347989Z hello world

2020-01-21T14:59:16.585383550Z hello world

2020-01-21T14:59:18.587162333Z hello world

2020-01-21T14:59:20.589211886Z hello world

2020-01-21T14:59:22.590984922Z hello world

2020-01-21T14:59:24.593126392Z hello world

2020-01-21T14:59:26.594956286Z hello world

2020-01-21T14:59:28.596946331Z hello world

2020-01-21T14:59:30.598956860Z hello world

2020-01-21T14:59:32.600943786Z hello world

2020-01-21T14:59:34.602621904Z hello world

2020-01-21T14:59:36.604524151Z hello world

2020-01-21T14:59:38.606559608Z hello world

2020-01-21T14:59:40.608289980Z hello world

2020-01-21T14:59:42.610326148Z hello world

2020-01-21T14:59:44.612038835Z hello world

2020-01-21T14:59:46.614093056Z hello world

2020-01-21T14:59:48.615917880Z hello world

2020-01-21T14:59:50.618115353Z hello world

2020-01-21T14:59:52.620334251Z hello world

^C

\[root@localhost ~\]\# docker logs -t --tail 5 06fb54229654

2020-01-21T15:03:14.817074652Z hello world

2020-01-21T15:03:16.818730588Z hello world

2020-01-21T15:03:18.820616778Z hello world

2020-01-21T15:03:20.822602287Z hello world

2020-01-21T15:03:22.824328662Z hello world

