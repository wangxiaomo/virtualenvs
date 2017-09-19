FROM php:7-apache

RUN apt-get update

RUN apt-get install -y libmcrypt-dev
RUN docker-php-ext-install mcrypt

RUN pecl install redis && docker-php-ext-enable redis
