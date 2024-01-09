FROM centos:centos7.9.2009

MAINTAINER johnlyon<liangzhanbo06@gmail.com>

RUN yum -y install wget

RUN wget -O /etc/yum.repos.d/CentOS7-Aliyun.repo http://mirrors.aliyun.com/repo/Centos-7.repo

RUN yum -y update && \
    yum -y install vim openssh-server openssh-clients && \
    ssh-keygen -A

RUN /usr/sbin/sshd

CMD ["/bin/bash", "-c", "/usr/sbin/sshd"]
