FROM php:7.4-apache

RUN apt update && apt install -y \
    git mariadb-client unzip \
    libpng-dev libjpeg-dev libfreetype6-dev libzip-dev \
    && docker-php-ext-install mysqli pdo pdo_mysql gd zip

RUN a2enmod rewrite

WORKDIR /var/www/html

RUN git clone https://github.com/lirantal/daloradius.git . \
    && chown -R www-data:www-data /var/www/html \
    && chmod -R 755 /var/www/html
