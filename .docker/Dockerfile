FROM php:8-fpm-alpine

WORKDIR /var/www/html

RUN docker-php-ext-install pdo pdo_mysql
RUN apk add --no-cache $PHPIZE_DEPS \
	&& pecl install xdebug-3.0.1 \
	&& docker-php-ext-enable xdebug
COPY xdebug.ini /usr/local/etc/php/conf.d/docker-php-ext-xdebug.ini
