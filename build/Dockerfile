FROM php:7.2-apache

RUN apt-get update && apt-get install -y wget unzip

ADD https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions /usr/local/bin/

RUN chmod +x /usr/local/bin/install-php-extensions && \
    install-php-extensions gd xdebug mysqli

RUN cd /var/www/html && \
 wget https://downloads.joomla.org/cms/joomla4/4-1-4/Joomla_4-1-4-Stable-Full_Package.zip?format=zip -O joomla.zip && \
 unzip joomla.zip  
