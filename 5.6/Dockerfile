FROM php:5.6
MAINTAINER Mike Milano <coder1@gmail.com>

RUN apt-get update && apt-get install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libmcrypt-dev \
        libpng12-dev \
    && docker-php-ext-install -j$(nproc) bcmath iconv mcrypt pdo_mysql zip \
    && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
    && docker-php-ext-install -j$(nproc) gd \
    && pecl install amqp \
    && usermod -u 1000 www-data \
    && mkdir -p /app

WORKDIR /app

ENTRYPOINT []
CMD []
