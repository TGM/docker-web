FROM php:fpm
RUN apt-get update && apt-get install -y \
	libzip-dev \
	libfreetype6-dev \
	libjpeg62-turbo-dev \
	libpng-dev \
 && docker-php-ext-configure gd --with-freetype --with-jpeg \
 && docker-php-ext-install -j$(nproc) bcmath mysqli pdo pdo_mysql zip gd
