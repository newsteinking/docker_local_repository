# Dockerfile for Docker Registry
# derived from https://github.com/dotcloud/docker-registry/blob/master/Dockerfile
# Version 1.0
FROM registry

MAINTAINER Lukas Pustina <lukas.pustina@codecentric.de>

ADD config.yml /etc/docker-registry/

VOLUME /docker-registry-storage

ENV DOCKER_REGISTRY_CONFIG /etc/docker-registry/config.yml
ENV SETTINGS_FLAVOR demo

## if you are in closed network add following proxy

#ENV http_proxy 'http://10.3.0.172:8080'
#ENV https_proxy 'http://10.3.0.172:8080'
#ENV HTTP_PROXY 'http://10.3.0.172:8080'
#ENV HTTPS_PROXY 'http://10.3.0.172:8080'
#RUN export http_proxy=$HTTP_PROXY
#RUN export https_proxy=$HTTPS_PROXY


ENV GUNICORN_WORKERS 8
ENV GUNICORN_GRACEFUL_TIMEOUT 3600
ENV GUNICORN_SILENT_TIMEOUT 3600
RUN sudo rm  -rvf /var/lib/apt/lists/*
RUN sudo sed 's@archive.ubuntu.com@ftp.kaist.ac.kr@' -i /etc/apt/sources.list
RUN sudo apt-get update

#CMD ["docker-registry"]
CMD ["private-docker"]

