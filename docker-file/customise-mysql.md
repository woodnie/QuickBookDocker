`docker run -p 3306:3306 --name mysql -v /mydockervolume/mysql5.6/conf:/etc/mysql/conf.d -v /mydockervolume/mysql5.6/logs:/logs -v /mydockervolume/mysql5.6/data:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=123456 -d mysql:5.6`

