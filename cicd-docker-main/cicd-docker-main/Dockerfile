FROM centos:7.9.2009
MAINTAINER siva.depur@gmail.com
RUN yum install -y httpd \
zip \
unzip
ADD https://www.free-css.com/assets/files/free-css-templates/download/page279/jack-and-rose.zip /var/www/html/
WORKDIR /var/www/html
RUN unzip jack-and-rose.zip
RUN cp -rvf free-wedding-website-template/* .
RUN rm -rf free-wedding-website-template jack-and-rose.zip
CMD ["/usr/sbin/httpd", "-D", "FOREGROUND"]
EXPOSE 80
