ARG PHP_VERSION=8.3.3
ARG COMPOSER_VERSION=2.6.2

FROM composer:${COMPOSER_VERSION} as composerbin

FROM php:${PHP_VERSION}-cli-alpine

COPY --from=composerbin /usr/bin/composer /usr/bin/composer
