FROM centos:7

RUN printf $'[mariadb]\n\
name=MariaDB\n\
baseurl=https://yum.mariadb.org/10.0/centos7-amd64\n\
gpgcheck=0\n' > /etc/yum.repos.d/mariadb.repo
RUN yum install -y initscripts cmake gcc-c++ boost-devel MariaDB-devel\
      zlib-devel openssl-devel MariaDB-server && yum clean all &&\
    rm -rf /tmp/* /var/tmp/* /var/cache/yum

