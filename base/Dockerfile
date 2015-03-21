# Dockerfile for python 
# Version 1.0
FROM ubuntu:14.04

MAINTAINER Lukas Pustina <lukas.pustina@codecentric.de>

ENV DEBIAN_FRONTEND noninteractive

RUN sudo rm -rvf /var/lib/apt/lists/* 
#RUN sudo sed 's@archive.ubuntu.com@ubuntu.mirror.atratoip.net@' -i /etc/apt/sources.list
RUN sudo sed 's@archive.ubuntu.com@ftp.kaist.ac.kr@' -i /etc/apt/sources.list
RUN sudo  apt-get update

