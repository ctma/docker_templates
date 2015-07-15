FROM centos:latest

MAINTAINER xgreddy@gmail.com

RUN yum install which curl-devel -y

RUN gpg2 --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3

COPY getrvm /root/getrvm

RUN cat /root/getrvm | bash -s stable --ruby
