FROM php:7.4.1-fpm-buster
LABEL maintainer="yurich84@gmail.com"

COPY ./laravel-cron.sh /usr/local/bin/laravel-cron
RUN chmod a+x /usr/local/bin/laravel-cron

# Installing dependencies
RUN apt-get update && apt-get install -y --no-install-recommends \
    build-essential \
    mariadb-client \
    libfreetype6-dev \
    libjpeg62-turbo-dev \
    libmcrypt-dev \
    libpng-dev \
    zlib1g-dev \
    libxml2-dev \
    libzip-dev \
    libonig-dev \
    graphviz \
    nano

# Clear cache
RUN apt-get clean && rm -rf /var/lib/apt/lists/*

# Installing extensions
RUN docker-php-ext-install pdo_mysql zip exif pcntl bcmath gd

WORKDIR /application