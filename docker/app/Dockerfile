FROM php:fpm-bullseye

# COPY php.ini
COPY ./docker/app/php.ini /usr/local/etc/php/php.ini

# Composer install
COPY --from=composer:2.4 /usr/bin/composer /usr/bin/composer

# install Node.js
COPY --from=node:lts-bullseye /usr/local/bin /usr/local/bin
COPY --from=node:lts-bullseye /usr/local/lib /usr/local/lib

RUN apt update && \
    apt -y install \
    git \
    zip \
    unzip \
    vim \
    && docker-php-ext-install pdo_mysql bcmath

WORKDIR /var/www/html