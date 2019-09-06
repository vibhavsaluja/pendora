#This is docker file for pendora MS frontend Layer
FROM centos:7
MAINTAINER vibhavsaluja@gmail.com
RUN yum -y update
ADD config /opt
RUN  yum -y install `cat /opt/packages`
RUN  yum -y install `cat /opt/my-packages`
ADD code /var/www/html
EXPOSE 80
ENV BACKENDLB=test
ADD script /usr/bin
RUN chmod 755 /usr/bin/startapache
CMD ["startapache"]
