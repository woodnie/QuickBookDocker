`[root@localhost mydockerfile]# docker build -f ./myip01_father -t myip01_father .`

`Sending build context to Docker daemon  6.144kB`

`Step 1/7 : from centos`

`---> 470671670cac`

`Step 2/7 : env http_proxy=http://zf-proxy.zf-world.com:8070`

`---> Using cache`

`---> 97687ad58c97`

`Step 3/7 : env https_proxy=http://zf-proxy.zf-world.com:8070`

`---> Using cache`

`---> 84628da11474`

`Step 4/7 : env ftp_proxy=http://zf-proxy.zf-world.com:8070`

`---> Using cache`

`---> db8507e2d697`

`Step 5/7 : run yum -y install curl`

`---> Using cache`

`---> 9379795fddee`

`Step 6/7 : entrypoint ["curl","-s","https://ip.cn/?ip=8.8.8.8"]`

`---> Using cache`

`---> 18987f853b97`

`Step 7/7 : onbuild run echo "******ONBUILD trigger*******"`

`---> Running in cde0b5252189`

`Removing intermediate container cde0b5252189`

`---> 29a8c8c9b6bd`

`Successfully built 29a8c8c9b6bd`

`Successfully tagged myip01_father:latest`

``

`[root@localhost mydockerfile]# docker build -f ./myip01_son -t myip01_son .`

`Sending build context to Docker daemon  6.144kB`

`Step 1/1 : from myip01_father`

`# Executing 1 build trigger`

`---> Running in b2c6e92b3e57`

`******ONBUILD trigger*******`

`Removing intermediate container b2c6e92b3e57`

`---> 37137016a03e`

`Successfully built 37137016a03e`

`Successfully tagged myip01_son:latest`

