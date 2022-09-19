FROM ubuntu:20.04

RUN apt update && apt upgrade -y  

RUN apt install openssh-server sudo -y 

RUN useradd -rm -d /home/ubuntu -s /bin/bash -g root -G sudo -u 1000 test

RUN echo 'test:test' | chpasswd

#RUN service ssh start

EXPOSE 22

ENTRYPOINT service ssh restart && bash

