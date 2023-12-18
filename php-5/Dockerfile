FROM php:7.2-fpm
RUN apt-get update \
  && docker-php-ext-install mysqli pdo pdo_mysql \
  && docker-php-ext-install opcache \
  && docker-php-ext-install bcmath \
  && docker-php-ext-install sockets \
  && docker-php-ext-install pcntl \
  && docker-php-ext-install exif \
  && docker-php-ext-install gettext \
  && docker-php-ext-install shmop \
  && docker-php-ext-install sysvmsg \
  && pecl install igbinary \
  && pecl install redis \
  && docker-php-ext-enable redis 
  

EXPOSE 9000