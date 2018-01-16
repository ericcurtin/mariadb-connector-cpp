FROM centos:6

RUN printf $'[mariadb]\n\
name=MariaDB\n\
baseurl=https://yum.mariadb.org/10.0/centos6-amd64\n\
gpgcheck=0\n' > /etc/yum.repos.d/mariadb.repo
RUN yum install -y upstart cmake gcc-c++ boost-devel MariaDB-devel &&\
    yum clean all &&\
    rm -rf /tmp/* /var/tmp/* /var/cache/yum

