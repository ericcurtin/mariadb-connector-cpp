FROM debian:8

ENV http_proxy=$http_proxy
ENV https_proxy=$https_proxy
ENV ftp_proxy=$ftp_proxy

RUN export DEBIAN_FRONTEND=noninteractive &&\
    apt update -y &&\
    apt install -y software-properties-common &&\
    apt-key adv --recv-keys --keyserver keyserver.ubuntu.com\
      0xcbcb082a1bb943db &&\
    add-apt-repository 'deb [arch=amd64]\
      http://ftp.heanet.ie/mirrors/mariadb/repo/10.0/debian jessie main' &&\
    apt update -y &&\
    apt install -y cmake g++ libboost-dev mariadb-server vim &&\
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

