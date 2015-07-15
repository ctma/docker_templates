FROM centos:latest

MAINTAINER xgreddy@gmail.com

RUN yum install wget -y

RUN wget http://apache.cs.utah.edu//ant/binaries/apache-ant-1.9.6-bin.tar.gz \
    && tar xzf apache-ant-1.9.6-bin.tar.gz \
    && ln -s apache-ant-1.9.6/bin/ant /usr/bin/ant

ADD wget http://mirror.cogentco.com/pub/apache/maven/maven-3/3.3.3/binaries/apache-maven-3.3.3-bin.tar.gz \
    && tar xzf apache-maven-3.3.3-bin.tar.gz \
    && ln -s apache-maven-3.3.3/bin/mvn /usr/bin/mvn

ENV JAVA_TOOL_OPTIONS -Dfile.encoding=UTF8

CMD ["/bin/bash", "-c", "eval $JENKINS_COMMAND"]

RUN yum install -y \
    git \
    rubygems \
