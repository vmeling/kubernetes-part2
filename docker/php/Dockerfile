FROM composer:latest AS composer
FROM php:8.0-fpm-alpine

COPY --from=composer /usr/bin/composer /usr/bin/composer

COPY . /var/www/arch.homework

RUN chown -R www-data:www-data /var/www/arch.homework

USER www-data

WORKDIR /var/www/arch.homework

RUN composer install --no-scripts

WORKDIR /var/www/arch.homework/public

