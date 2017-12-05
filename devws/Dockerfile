################################################################
# Dockerfile to build personal devellopment workstations images
#
# Based on CentOS 6.9
################################################################

FROM centos:6.9
MAINTAINER ericlichen
RUN yum update -y

############### Add Necessary Repo Files ######################
RUN yum install epel-release -y
RUN yum install openssh-clients -y
RUN yum install vim -y
RUN yum install git -y
RUN yum install ansible -y
RUN yum install java-1.8.0-openjdk java-1.8.0-openjdk-devel -y
