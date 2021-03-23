FROM php:7.4-fpm

COPY php.ini /usr/local/etc/php

RUN apt-get update -y \
    && apt-get install -y zlib1g-dev zip \
    && docker-php-ext-install pdo_mysql

# set environment variable 環境変数設定
ENV COMPOSER_ALLOW_SUPERUSER 1

ENV COMPOSER_HOME /

ENV PATH $PATH=/composer/vendor/bin

WORKDIR /var/www
