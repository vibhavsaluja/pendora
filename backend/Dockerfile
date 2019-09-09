#This is docker file for pendora MS frontend Layer
FROM centos:7
MAINTAINER vibhavsaluja@gmail.com
RUN yum -y update
RUN yum -y install httpd php php-gd php-mysql
ADD config /opt
RUN  yum -y install `cat /opt/packages`
RUN  yum -y install `cat /opt/my-packages`
ADD code /var/www/html
EXPOSE 80
ENV BACKENDLB=test MY_DB_HOST=test MY_DB_NAME_WRITE=test MY_DB_USER=test MY_DB_PASS=test MY_DB_NAME_READ=test
ADD script /usr/bin
RUN chmod 755 /usr/bin/startapache
CMD ["startapache"]
