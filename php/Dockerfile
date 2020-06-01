FROM php:7.3.3-apache
RUN apt-get update && apt-get upgrade -y
RUN docker-php-ext-install mysqli
RUN mkdir /var/www-data
ADD netsim.db /var/www-data/netsim.db
RUN apt-get install -y software-properties-common python
RUN echo "deb http://us.archive.ubuntu.com/ubuntu/ precise universe" >> /etc/apt/sources.list
RUN apt-get update
RUN apt-get install -y nodejs
RUN chown www-data:www-data /var/www/html/
RUN chown www-data:www-data /var/www-data/
RUN chmod 777 /var/www-data/netsim.db
EXPOSE 80
