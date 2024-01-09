FROM arm64v8/centos

MAINTAINER johnlyon<liangzhanbo06@gmail.com>

RUN sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-* && \
sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*

RUN yum clean all && \
    yum -y update && \
    yum -y install vim openssh-server openssh-clients passwd && \
    ssh-keygen -A

CMD ["/bin/bash", "-c", "/usr/sbin/sshd"]
