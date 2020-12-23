FROM php:7.3-fpm-alpine

COPY ./build-api /api

WORKDIR "/app"

ENTRYPOINT ["docker-php-entrypoint"]
CMD ["php-fpm"]