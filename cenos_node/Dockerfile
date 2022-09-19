FROM centos/systemd

#MAINTAINER "Your Name" <you@example.com>

#RUN yum -y install openssh-server; yum clean all; systemctl enable sshd.service

RUN yum -y install openssh-server; yum clean all

RUN yum install sudo -y

RUN useradd -m -d /home/ubuntu -s /bin/bash test 

RUN echo 'test:test' | chpasswd

RUN usermod -aG wheel test

RUN systemctl enable sshd.service

EXPOSE 80

CMD ["/usr/sbin/init"]
