FROM composer:2.8.0 as composer_bin

FROM php:8.3.12-cli-alpine

COPY --from=composer_bin /usr/bin/composer /usr/bin/composer
COPY composer.* /usr/local/src/

WORKDIR /usr/local/src/

ENV PATH /usr/local/src/vendor/bin:$PATH

RUN composer install --optimize-autoloader