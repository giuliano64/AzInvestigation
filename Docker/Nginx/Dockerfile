FROM centos:centos7
LABEL maintainer="fgceliberti@gmail.com"

RUN yum -y install epel-release
RUN yum -y update
RUN yum -y install nginx

COPY nginx.conf /etc/nginx/nginx.conf
COPY index.html /usr/share/nginx/html/index.html
VOLUME [ "/data/www" ]
EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]