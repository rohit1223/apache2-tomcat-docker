# apache2-tomcat-docker
Apache2 Tomcat docker configuration

This repo contains docker image source for `dshot/docker-httpd-tomcat_web` and `dshot/docker-httpd-tomcat_http` and ansible files to achieve a 3 tire web application where all the static contents are hosted on `http` server and application content is hosted on `tomcat` server.
For convenience and demo purposes in-file database `Prevayler` is being used for persistence.

To check ansible configuration go to `ansible_playbook` and read `README.md` present inside it.
