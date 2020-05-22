```
[root@localhost mydockerfile]# docker build -f ./dockerfile2 -t newcentos:1.0 ./
Sending build context to Docker daemon 3.072kB
Step 1/13 : from centos

---> 470671670cac

Step 2/13 : maintainer wood.nie@zf.com

---> Using cache

---> 85931063dd96

Step 3/13 : env mypath /tmp

---> Using cache

---> 249703701931

Step 4/13 : env http_proxy=http://zf-proxy.zf-world.com:8070

---> Using cache

---> 4f05d76222ef

Step 5/13 : env https_proxy=http://zf-proxy.zf-world.com:8070

---> Using cache

---> d9f1e712e71d

Step 6/13 : env ftp_proxy=http://zf-proxy.zf-world.com:8070

---> Using cache

---> 13bb36414219

Step 7/13 : workdir $mypath

---> Using cache

---> 201955bfe97b

Step 8/13 : run yum -y install vim

---> Running in 5d3253f2cbec

CentOS-8 - AppStream 514 kB/s | 6.0 MB 00:11

CentOS-8 - Base 276 kB/s | 4.0 MB 00:14

CentOS-8 - Extras 1.7 kB/s | 2.1 kB 00:01

Dependencies resolved.

================================================================================

Package Arch Version Repository Size

================================================================================

Installing:

vim-enhanced x86_64 2:8.0.1763-13.el8 AppStream 1.4 M

Installing dependencies:

gpm-libs x86_64 1.20.7-15.el8 AppStream 39 k

vim-common x86_64 2:8.0.1763-13.el8 AppStream 6.3 M

vim-filesystem noarch 2:8.0.1763-13.el8 AppStream 48 k

which x86_64 2.21-10.el8 BaseOS 49 k


Transaction Summary

================================================================================

Install 5 Packages


Total download size: 7.8 M

Installed size: 31 M

Downloading Packages:

(1/5): gpm-libs-1.20.7-15.el8.x86_64.rpm 36 kB/s | 39 kB 00:01

(2/5): vim-filesystem-8.0.1763-13.el8.noarch.rp 96 kB/s | 48 kB 00:00

(3/5): vim-enhanced-8.0.1763-13.el8.x86_64.rpm 127 kB/s | 1.4 MB 00:10

[MIRROR] which-2.21-10.el8.x86_64.rpm: Status code: 403 for http://ftp.twaren.net/Linux/CentOS/8.1.1911/BaseOS/x86_64/os/Packages/which-2.21-10.el8.x86_64.rpm

(4/5): which-2.21-10.el8.x86_64.rpm 3.5 kB/s | 49 kB 00:14

(5/5): vim-common-8.0.1763-13.el8.x86_64.rpm 267 kB/s | 6.3 MB 00:24

--------------------------------------------------------------------------------

Total 321 kB/s | 7.8 MB 00:25

warning: /var/cache/dnf/AppStream-02e86d1c976ab532/packages/gpm-libs-1.20.7-15.el8.x86_64.rpm: Header V3 RSA/SHA256 Signature, key ID 8483c65d: NOKEY

CentOS-8 - AppStream 1.6 MB/s | 1.6 kB 00:00

Importing GPG key 0x8483C65D:

Userid : "CentOS (CentOS Official Signing Key) <security@centos.org>"

Fingerprint: 99DB 70FA E1D7 CE22 7FB6 4882 05B5 55B3 8483 C65D

From : /etc/pki/rpm-gpg/RPM-GPG-KEY-centosofficial

Key imported successfully

Running transaction check

Transaction check succeeded.

Running transaction test

Transaction test succeeded.

Running transaction

Preparing : 1/1

Installing : which-2.21-10.el8.x86_64 1/5

Installing : vim-filesystem-2:8.0.1763-13.el8.noarch 2/5

Installing : vim-common-2:8.0.1763-13.el8.x86_64 3/5

Installing : gpm-libs-1.20.7-15.el8.x86_64 4/5

Running scriptlet: gpm-libs-1.20.7-15.el8.x86_64 4/5

Installing : vim-enhanced-2:8.0.1763-13.el8.x86_64 5/5

Running scriptlet: vim-enhanced-2:8.0.1763-13.el8.x86_64 5/5

Running scriptlet: vim-common-2:8.0.1763-13.el8.x86_64 5/5

Verifying : gpm-libs-1.20.7-15.el8.x86_64 1/5

Verifying : vim-common-2:8.0.1763-13.el8.x86_64 2/5

Verifying : vim-enhanced-2:8.0.1763-13.el8.x86_64 3/5

Verifying : vim-filesystem-2:8.0.1763-13.el8.noarch 4/5

Verifying : which-2.21-10.el8.x86_64 5/5


Installed:

vim-enhanced-2:8.0.1763-13.el8.x86_64 gpm-libs-1.20.7-15.el8.x86_64

vim-common-2:8.0.1763-13.el8.x86_64 vim-filesystem-2:8.0.1763-13.el8.noarch

which-2.21-10.el8.x86_64


Complete!

Removing intermediate container 5d3253f2cbec

---> bf003c52ac96

Step 9/13 : run yum -y install net-tools

---> Running in 2871fb448ee4

Last metadata expiration check: 0:00:40 ago on Sun Feb 2 03:16:56 2020.

Dependencies resolved.

================================================================================

Package Architecture Version Repository Size

================================================================================

Installing:

net-tools x86_64 2.0-0.51.20160912git.el8 BaseOS 323 k


Transaction Summary

================================================================================

Install 1 Package


Total download size: 323 k

Installed size: 1.0 M

Downloading Packages:

[MIRROR] net-tools-2.0-0.51.20160912git.el8.x86_64.rpm: Status code: 403 for http://ftp.twaren.net/Linux/CentOS/8.1.1911/BaseOS/x86_64/os/Packages/net-tools-2.0-0.51.20160912git.el8.x86_64.rpm

net-tools-2.0-0.51.20160912git.el8.x86_64.rpm 87 kB/s | 323 kB 00:03

--------------------------------------------------------------------------------

Total 72 kB/s | 323 kB 00:04

Running transaction check

Transaction check succeeded.

Running transaction test

Transaction test succeeded.

Running transaction

Preparing : 1/1

Installing : net-tools-2.0-0.51.20160912git.el8.x86_64 1/1

Running scriptlet: net-tools-2.0-0.51.20160912git.el8.x86_64 1/1

Verifying : net-tools-2.0-0.51.20160912git.el8.x86_64 1/1


Installed:

net-tools-2.0-0.51.20160912git.el8.x86_64


Complete!

Removing intermediate container 2871fb448ee4

---> f76996945a7e

Step 10/13 : expose 80

---> Running in 0254f83e2f55

Removing intermediate container 0254f83e2f55

---> 7925618afbca

Step 11/13 : cmd echo $mypath

---> Running in 69f85ef2c8c2

Removing intermediate container 69f85ef2c8c2

---> d85ea90fba58

Step 12/13 : cmd echo "success....."

---> Running in 915cc46431a6

Removing intermediate container 915cc46431a6

---> d60ef15445fe

Step 13/13 : cmd /bin/bash

---> Running in 44e2aed9d3d7

Removing intermediate container 44e2aed9d3d7

---> 231f955eaf27

Successfully built 231f955eaf27

Successfully tagged newcentos:1.0

```