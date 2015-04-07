# Dockerfile for python 
# Version 1.0
FROM ubuntu:14.04

MAINTAINER Lukas Pustina <lukas.pustina@codecentric.de>

ENV DEBIAN_FRONTEND noninteractive

ENV http_proxy 'http://10.3.0.172:8080'
ENV https_proxy 'http://10.3.0.172:8080'
ENV HTTP_PROXY 'http://10.3.0.172:8080'
ENV HTTPS_PROXY 'http://10.3.0.172:8080'
RUN export http_proxy=$HTTP_PROXY
RUN export https_proxy=$HTTPS_PROXY


RUN sudo rm -rvf /var/lib/apt/lists/* 
#RUN sudo sed 's@archive.ubuntu.com@ubuntu.mirror.atratoip.net@' -i /etc/apt/sources.list
RUN sudo sed 's@archive.ubuntu.com@ftp.kaist.ac.kr@' -i /etc/apt/sources.list
RUN sudo  apt-get update

