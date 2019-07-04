#Download base image ubuntu 16.04
FROM ubuntu:16.04

# Update Ubuntu Software repository
RUN apt-get update -y

# Install nginx, php-fpm and supervisord from ubuntu repository
RUN apt-get install -y nginx

RUN apt-get clean

RUN rm -frv /var/www/html/*

COPY index.html /var/www/html/index.html

RUN chmod +r /var/www/html/index.html



EXPOSE 8080

CMD ["nginx", "-g", "daemon off;"]
