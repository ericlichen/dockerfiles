################################################################
# Dockerfile to build personal devellopment workstations images
#
# Based on CentOS 6.9
################################################################

FROM centos:6.9
MAINTAINER ericlichen
RUN yum update -y

############### Add Necessary RPMS ######################
RUN yum install epel-release -y
RUN yum install openssh-clients -y
RUN yum install vim -y
RUN yum install git -y
RUN yum install ansible -y
RUN yum install java-1.8.0-openjdk java-1.8.0-openjdk-devel -y
RUN echo $JAVA_HOME

############### Install Maven  ######################
ARG MAVEN_TAR="apache-maven-3.5.2-bin.tar.gz"
ADD http://apache.mirror.digitalpacific.com.au/maven/maven-3/3.5.2/binaries/${MAVEN_TAR} /tmp
RUN rm -rf /opt/maven
RUN mkdir /opt/maven
RUN tar xvf /tmp/${MAVEN_TAR} -C /opt/maven


############### Mount Volume  ######################
RUN mkdir /root/workspace
ADD . /root/workspace
