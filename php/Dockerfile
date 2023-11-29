FROM php:8.2-fpm
RUN apt-get update && apt-get install -y \
		libfreetype-dev \
		libjpeg62-turbo-dev \
		libpng-dev \
	&& docker-php-ext-configure gd --with-freetype --with-jpeg \
	&& docker-php-ext-install -j$(nproc) gd \
  && docker-php-ext-install mysqli pdo pdo_mysql \
  && docker-php-ext-install opcache \
  && docker-php-ext-install bcmath \
  && docker-php-ext-install sockets \
  && docker-php-ext-install pcntl \
  && docker-php-ext-install exif \
  && docker-php-ext-install gettext \
  && docker-php-ext-install shmop \
  && docker-php-ext-install sysvmsg \
  && pecl install redis \
  && pecl install xdebug \
  && docker-php-ext-enable redis \
  && docker-php-ext-enable xdebug 

EXPOSE 9000