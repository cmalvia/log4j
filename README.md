# Apache Log4j cve example repo and docker images

This repository holds code to reproduce the [Log4j cve](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-44228) 


17:22:20.369 [main] ERROR MyExample - if you can read this this code is vulnerable
```
The code above is using log4j `2.14.1` which is vulnerable.

There is an image [cmalvia/my-app:log4jv1](https://hub.docker.com/repository/docker/cmalvia/my-app) that you can get from Docker Hub which holds the code of this repository.

## Working around the vulnerability
With this repo you can play with possible workarounds and fixes, notably by moving to `2.15.0` of log4j, you can do this in the [pom.xml](pom.xml#L18) or you can experiment with the `LOG4J_FORMAT_MSG_NO_LOOKUPS=true` environment variable that you can test in the included [Dockerfile](Dockerfile#L8)

Code modified from Packet Storm
https://packetstormsecurity.com/files/download/165225/apache-log4j-poc-main.zip

