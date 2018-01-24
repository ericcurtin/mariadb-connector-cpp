FROM ubuntu:16.04

ENV http_proxy=$http_proxy
ENV https_proxy=$https_proxy
ENV ftp_proxy=$ftp_proxy

RUN export DEBIAN_FRONTEND=noninteractive &&\
    apt update -y &&\
    apt install -y software-properties-common &&\
    apt-key adv --recv-keys --keyserver\
      hkp://keyserver.ubuntu.com:80 0xF1656F24C74CD1D8 &&\
    add-apt-repository 'deb [arch=amd64]\
      http://ftp.heanet.ie/mirrors/mariadb/repo/10.0/ubuntu xenial main' &&\
    apt update -y &&\
    apt install -y cmake g++ libboost-dev mariadb-server vim &&\
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /var/lib/mysql/*

