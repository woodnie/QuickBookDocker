`[root@localhost mydockerfile]# cat myip01`

`from centos`

`env http_proxy=http://zf-proxy.zf-world.com:8070`

`env https_proxy=http://zf-proxy.zf-world.com:8070`

`env ftp_proxy=http://zf-proxy.zf-world.com:8070`

`run yum -y install curl`

`entrypoint ["curl","-s","https://ip.cn/?ip=8.8.8.8"]`

``

`[root@localhost mydockerfile]# docker build -f ./myip01 -t myip01 .`

`Sending build context to Docker daemon  4.096kB`

`Step 1/6 : from centos`

`---> 470671670cac`

`Step 2/6 : env http_proxy=http://zf-proxy.zf-world.com:8070`

`---> Running in 9db1ec5a9283`

`Removing intermediate container 9db1ec5a9283`

`---> 97687ad58c97`

`Step 3/6 : env https_proxy=http://zf-proxy.zf-world.com:8070`

`---> Running in 1f27031339a0`

`Removing intermediate container 1f27031339a0`

`---> 84628da11474`

`Step 4/6 : env ftp_proxy=http://zf-proxy.zf-world.com:8070`

`---> Running in b9a05174a1ef`

`Removing intermediate container b9a05174a1ef`

`---> db8507e2d697`

`Step 5/6 : run yum -y install curl`

`---> Running in f0ed8dfb073e`

`CentOS-8 - AppStream                            623 kB/s | 6.0 MB     00:09`

`CentOS-8 - Base                                 272 kB/s | 4.0 MB     00:15`

`CentOS-8 - Extras                                76  B/s | 2.1 kB     00:28`

`Last metadata expiration check: 0:00:02 ago on Sun Feb  2 07:31:35 2020.`

`Package curl-7.61.1-11.el8.x86_64 is already installed.`

`Dependencies resolved.`

`Nothing to do.`

`Complete!`

`Removing intermediate container f0ed8dfb073e`

`---> 9379795fddee`

`Step 6/6 : entrypoint ["curl","-s","https://ip.cn/?ip=8.8.8.8"]`

`---> Running in b828632c6f80`

`Removing intermediate container b828632c6f80`

`---> 18987f853b97`

`Successfully built 18987f853b97`

`Successfully tagged myip01:latest`

``

`[root@localhost mydockerfile]# docker run myip01 -i`

`HTTP/1.1 200 Connection established`

``

`HTTP/2 200`

`date: Sun, 02 Feb 2020 07:38:44 GMT`

`content-type: application/json; charset=UTF-8`

`set-cookie: __cfduid=d2bf5d73ed9e35b391fc7b56cacaf87b21580629122; expires=Tue, 03-Mar-20 07:38:42 GMT; path=/; domain=.ip.cn; HttpOnly; SameSite=Lax`

`cf-cache-status: DYNAMIC`

`expect-ct: max-age=604800, report-uri="https://report-uri.cloudflare.com/cdn-cgi/beacon/expect-ct"`

`server: cloudflare`

`cf-ray: 55ea81d15ec1a366-HKG`

``

`{"ip": "8.8.8.8", "country": "Google", "city": "DNS"}`

`[root@localhost mydockerfile]#`

