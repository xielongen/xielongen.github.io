FROM ubuntu:14.04
MAINTAINER longen "x@xxxx.com"

RUN sed -i "s/archive.ubuntu.com/ubuntu.uhost.hk/g" /etc/apt/sources.list
RUN apt-get update
RUN apt-get -y upgrade
#RUN apt-get -y install vim wget git
RUN apt-get -y install python python-dev python-pip
RUN apt-get -y build-dep python-matplotlib 
ADD requirements.txt /tmp/
RUN pip install -U -r /tmp/requirements.txt
WORKDIR /root/
VOLUME ["/home/x"]
