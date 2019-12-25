FROM php:7.3-fpm-stretch
LABEL maintainer="guillaumebriday@gmail.com"

# Installing dependencies
RUN apt-get update && apt-get install -y --no-install-recommends \
    build-essential \
    mysql-client \
    libpng-dev \
    libjpeg62-turbo-dev \
    libfreetype6-dev \
    libmagickwand-dev \
    libzip-dev \
    zip \
    jpegoptim optipng pngquant gifsicle

# Clear cache
RUN apt-get clean && rm -rf /var/lib/apt/lists/*

# Installing extensions
RUN docker-php-ext-install pdo_mysql mbstring zip exif pcntl bcmath opcache

# Changing Workdir
WORKDIR /application