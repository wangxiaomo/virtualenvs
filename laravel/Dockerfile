FROM php:7-apache

RUN apt-get update
RUN apt-get install -y zip unzip

RUN apt-get install -y libmcrypt-dev
RUN docker-php-ext-install mcrypt

RUN apt-get install -y libfreetype6-dev libjpeg62-turbo-dev libpng12-dev
RUN docker-php-ext-install iconv
RUN docker-php-ext-configure gd --with-freetype-dir=/usr/include --with-jpeg-dir=/usr/include && docker-php-ext-install gd

RUN docker-php-ext-install pdo pdo_mysql
RUN docker-php-ext-install mysqli

WORKDIR /root
RUN php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
RUN php composer-setup.php
RUN php -r "unlink('composer-setup.php');" && cp composer.phar /usr/local/bin/composer
RUN chmod 755 /usr/local/bin/composer

COPY apache2 /etc/apache2
COPY php.ini /usr/local/etc/php

WORKDIR /var/www/html
