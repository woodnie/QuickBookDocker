# docker file:

`[root@localhost mytomcat9]# cat mytomcat9`

`FROM         centos`

`MAINTAINER    <wood.nie@zf.com>`

`#把宿主机当前上下文的c.txt拷贝到容器/usr/local/路径下`

`COPY c.txt /usr/local/cincontainer.txt`

`#把java与tomcat添加到容器中`

`ADD openjdk-9_linux-x64_bin.tar.gz /usr/local/`

`ADD apache-tomcat-9.0.8.tar.gz /usr/local/`

`RUN chown root:root /usr/local/jdk-9`

`RUN alias ll='ls -l --color=auto'`

`#设置工作访问时候的WORKDIR路径，登录落脚点`

`ENV MYPATH /usr/local`

`WORKDIR $MYPATH`

`#配置java与tomcat环境变量`

`ENV JAVA_HOME /usr/local/openjdk-9`

`ENV CLASSPATH $JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar`

`ENV CATALINA_HOME /usr/local/apache-tomcat-9.0.8`

`ENV CATALINA_BASE /usr/local/apache-tomcat-9.0.8`

`ENV PATH $PATH:$JAVA_HOME/bin:$CATALINA_HOME/lib:$CATALINA_HOME/bin`

`#容器运行时监听的端口`

`EXPOSE  8080`

`#启动时运行tomcat`

`# ENTRYPOINT ["/usr/local/apache-tomcat-9.0.8/bin/startup.sh" ]`

`# CMD ["/usr/local/apache-tomcat-9.0.8/bin/catalina.sh","run"]`

`CMD /usr/local/apache-tomcat-9.0.8/bin/startup.sh && tail -F /usr/local/apache-tomcat-9.0.8/bin/logs/catalina.out`

# docker run:

`docker run -d -p 8080:8080  -v /mydockerfile/mytomcat9/test:/usr/local/apache-tomcat-9.0.8/webapps/test -v /mydockerfile/mytomcat9/tomcat9logs/:/usr/local/apache-tomcat-9.0.8/logs  mytomcat9`

# Sample Web application:

`[root@localhost test]# pwd`

`/mydockerfile/mytomcat9/test`

`[root@localhost test]# ll`

`total 4`

`-rw-r--r--. 1 root root 508 Feb  3 22:02 a.jsp`

`drwxr-xr-x. 2 root root  21 Feb  3 22:02 WEB-INF`

`[root@localhost test]# ll WEB-INF/`

`total 4`

`-rw-r--r--. 1 root root 337 Feb  3 22:02 web.xml`

`[root@localhost test]#`

## web.xml

`<?xml version="1.0" encoding="UTF-8"?>`

`<web-app xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"`

`xmlns="http://java.sun.com/xml/ns/javaee"`

`xsi:schemaLocation="http://java.sun.com/xml/ns/javaee http://java.sun.com/xml/ns/javaee/web-app_2_5.xsd"`

`id="WebApp_ID" version="2.5">`

`<display-name>test</display-name>`

`</web-app>`

## a.jsp

`<%@ page language="java" contentType="text/html; charset=UTF-8" pageEncoding="UTF-8"%>`

`<!DOCTYPE html PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">`

`<html>`

`<head>`

`<meta http-equiv="Content-Type" content="text/html; charset=UTF-8">`

`<title>Insert title here</title>`

`</head>`

`<body>`

`-----------welcome------------`

`<%="i am in docker tomcat self "%>`

`<br>`

`<br>`

`<% System.out.println("=============docker tomcat self");%>`

`</body>`

`</html>`

