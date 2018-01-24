FROM debian:8

RUN apt update -y &&\
    apt install -y software-properties-common &&\
    apt-key adv --recv-keys --keyserver keyserver.ubuntu.com\
      0xcbcb082a1bb943db &&\
    add-apt-repository 'deb [arch=amd64,i386,ppc64el]\
      http://ftp.heanet.ie/mirrors/mariadb/repo/10.0/debian jessie main' &&\
    apt update -y &&\
    apt install -y cmake g++ libboost-dev mariadb-server vim &&\
    rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

