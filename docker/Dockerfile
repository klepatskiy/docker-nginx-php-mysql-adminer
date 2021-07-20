FROM php:8.0-fpm

# Install system dependencies
RUN apt-get update && apt-get install -y git

# Install PHP extensions
RUN docker-php-ext-install pdo_mysql
RUN docker-php-ext-install sockets
RUN docker-php-ext-configure sockets
RUN docker-php-ext-enable sockets
RUN docker-php-ext-install mysqli
RUN docker-php-ext-enable mysqli

RUN apt-get install -y \
        libzip-dev \
        zip \
  && docker-php-ext-install zip

# Get latest Composer
COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

# Set working directory
WORKDIR /var/www