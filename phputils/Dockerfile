FROM composer:2.7.1 as composer_bin

FROM php:8.3.3-cli-alpine

COPY --from=composer_bin /usr/bin/composer /usr/bin/composer
