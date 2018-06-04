################################################################
# Docker file to build personal development workstations images
#
# Based on debian
################################################################

FROM debian
MAINTAINER ericlichen
RUN apt-get update

############### Add Necessary Packages ######################
RUN apt-get install vim -y
RUN apt-get install gpg -y
RUN apt-get install curl -y
RUN apt-get install -y procps
RUN curl -sSL https://rvm.io/mpapis.asc | gpg --import -
RUN curl -sSL https://get.rvm.io | bash -s stable --ruby
RUN source /etc/profile.d/rvm.sh
RUN rvm use ruby


############### Mount Volume  ######################
RUN mkdir -p /root/workspace
ADD . /root/workspace
