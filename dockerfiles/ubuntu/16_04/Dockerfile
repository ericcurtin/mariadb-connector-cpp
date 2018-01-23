FROM ubuntu:16.04

RUN apt-key adv --recv-keys --keyserver\
      hkp://keyserver.ubuntu.com:80 0xF1656F24C74CD1D8 &&\
    add-apt-repository 'deb [arch=amd64,i386,ppc64el]\
      http://ftp.heanet.ie/mirrors/mariadb/repo/10.0/ubuntu xenial main' &&\
    apt update -y &&\
    apt install -y cmake g++ libboost-dev mariadb-server &&\
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

