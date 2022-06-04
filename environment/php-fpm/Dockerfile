FROM php:fpm

#install requirements and aditional extensions	
RUN apt-get update && apt-get install -y \
	unzip

RUN curl -sSLf \
        -o /usr/local/bin/install-php-extensions \
        https://github.com/mlocati/docker-php-extension-installer/releases/latest/download/install-php-extensions && \
    chmod +x /usr/local/bin/install-php-extensions && \
    install-php-extensions bcmath gmp pdo_mysql zip @composer
