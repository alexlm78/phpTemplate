FROM php:fpm-alpine
RUN docker-php-ext-install opcache
COPY php/opcache.ini /usr/local/etc/php/conf.d/opcache.ini
COPY ./app/ /var/www/html/
