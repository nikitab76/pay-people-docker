FROM php:8.2-fpm

#RUN docker-php-ext-install pdo mysqli pdo_mysql zip

# Install apks
RUN apt-get update && apt-get install -y \
    curl \
    libpng-dev \
    libonig-dev \
    libxml2-dev \
    libzip-dev \
    libpq-dev \
    nano \
    mc
RUN apt-get clean && rm -rf /var/lib/apt/lists/*

# Install PHP extensions
RUN docker-php-ext-install pdo_mysql mbstring pcntl sockets zip

COPY --from=composer /usr/bin/composer /usr/bin/composer

# RUN apt-get update && apt-get install -y \
#     git \
#     curl \
#     zip \
#     vim \
#     unzip
