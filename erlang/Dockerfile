FROM centos:latest

MAINTAINER xgreddy@gmail.com

RUN yum install -y \
    tar \
    epel-release

RUN yum install -y erlang

ENV JAVA_OPTS -Xdebug -Xnoagent -Djava.compiler=NONE -Xrunjdwp:transport=dt_socket,address=8000,server=y,suspend=n -XX:PermSize=512m -Xmx2g

ENV MAVEN_OPTS -Xmx1g -XX:PermSize=512m
