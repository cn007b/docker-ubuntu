FROM ubuntu:18.04

MAINTAINER V.K. <cn007b@gmail.com>

ENV TERM=xterm
ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update --fix-missing

RUN apt-get install -y vim tree mc
RUN apt-get install -y git colordiff
RUN apt-get install -y curl net-tools telnet ftp nmap
RUN apt-get install -y unzip
# RUN apt-get install -y libpcre3-dev
RUN apt-get install -y make
RUN apt-get update --fix-missing && apt-get install -y lsb-core
RUN apt-get install -y uuid
RUN apt-get install -y jq

# docker
RUN apt-get install -y docker.io

# aws
RUN mkdir -p /root/.aws/ \
    && echo '[default]\nregion = eu-central-1' > /root/.aws/credentials \
    && apt-get install -y awscli

# ApacheBench
RUN apt-get update --fix-missing &&  apt-get install -y apache2-utils

# ZeroMQ
RUN apt-get install -y libzmq5 libzmq5-dev

# Monitoring
RUN apt-get install -y dstat
RUN apt-get install -y sysstat
# RUN apt-get install -y iotop
RUN apt-get install -y cbm

RUN apt-get clean
