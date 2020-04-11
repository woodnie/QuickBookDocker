* **Method 1 : Configuring proxy variables in the /etc/sysconfig/docker file**

Add following configuration in /etc/sysconfig/docker file:

\# cat /etc/sysconfig/docker

export HTTP\_PROXY="[http://USERNAME:PASSWORD@\[your.proxy.server\]:\[port\](http://USERNAME:PASSWORD@[your.proxy.server]:[port\)\]"

export HTTPS\_PROXY="[https://USERNAME:PASSWORD@\[your.proxy.server\]:\[port\](https://USERNAME:PASSWORD@[your.proxy.server]:[port\)\]"

For example :

\# cat /etc/sysconfig/docker

HTTP\_PROXY="[http://user01:password@10.10.10.10:8080](http://user01:password@10.10.10.10:8080)"

HTTPS\_PROXY="[https://user01:password@10.10.10.10:8080](https://user01:password@10.10.10.10:8080)"

1. Restart the Docker daemon after setting up the proxy.

\# service docker restart

* **Method 2 : Configuring environment variables**

Create a drop-in

\# mkdir /etc/systemd/system/docker.service.d

1. Create a file with name /etc/systemd/system/docker.service.d/http-proxy.conf that adds the HTTP\_PROXY environment variable:

\[Service\]

Environment="HTTP\_PROXY=[http://user01:password@10.10.10.10:8080/](http://user01:password@10.10.10.10:8080/)"

Environment="HTTPS\_PROXY=[https://user01:password@10.10.10.10:8080/](https://user01:password@10.10.10.10:8080/)"

Environment="NO\_PROXY= hostname.example.com,172.10.10.10"

1. reload the systemd daemon

\# systemctl daemon-reload

1. restart docker

\# systemctl restart docker

1. Verify that the configuration has been loaded:

\# systemctl show docker --property Environment

Environment=GOTRACEBACK=crash HTTP\_PROXY=[http://10.10.10.10:8080/](http://10.10.10.10:8080/) HTTPS\_PROXY=[http://10.10.10.10:8080/](http://10.10.10.10:8080/) NO\_PR

