FROM composer:2.8.8 as composer_bin

FROM php:8.4.6-cli-alpine

COPY --from=composer_bin /usr/bin/composer /usr/bin/composer
COPY composer.* /usr/local/src/

WORKDIR /usr/local/src/

ENV PATH /usr/local/src/vendor/bin:$PATH

RUN composer install --optimize-autoloader