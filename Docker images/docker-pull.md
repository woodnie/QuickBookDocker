\[root@localhost ~\]\# docker pull --help

Usage:  docker pull \[OPTIONS\] NAME\[:TAG\|@DIGEST\]

Pull an image or a repository from a registry

Options:

-a, --all-tags                Download all tagged images in the repository

```
  --disable-content-trust   Skip image verification \(default true\)
```

-q, --quiet                   Suppress verbose output

\[root@localhost ~\]\# docker pull tomcat /\* ==docker pull tomcat:latest

\[root@localhost ~\]\# docker pull tomcat:latest

\[root@localhost ~\]\# docker pull centos

