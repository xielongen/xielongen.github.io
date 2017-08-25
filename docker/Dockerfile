FROM ubuntu:16.04
#####################################################################
RUN sed -i "s/archive.ubuntu.com/mirrors.aliyun.com/g" /etc/apt/sources.list && apt-get update && apt-get -y upgrade
#####################################################################
RUN apt-get -y install vim wget curl git libffi-dev libssl-dev
#####################################################################
RUN apt-get -y install python python-dev python-pip ipython python3 python3-dev python3-pip ipython3

RUN mkdir /root/.pip
ADD pip.conf /root/.pip/pip.conf
RUN pip install --upgrade pip && pip3 install --upgrade pip

# system
RUN pip install psutil

# meta
RUN pip install meta astunparse

# performance
RUN pip install line-profiler Cython

# base
RUN pip install cffi cryptography lz4 chardet requests Jinja2

# common
RUN pip install configparser nose coverage

# data science
RUN apt-get -y build-dep python-numpy python-scipy python-pandas python-matplotlib
RUN pip install numpy scipy pandas==0.19 matplotlib

# service
RUN pip install pymongo PyMySQL pyOpenSSL pyzmq redis sqlalchemy

# web
RUN pip install beautifulsoup4 Flask
