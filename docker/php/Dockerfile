FROM php:7.3-alpine

ENV COMPOSER_ALLOW_SUPERUSER 1
COPY --from=composer /usr/bin/composer /usr/bin/composer

ENV PATH $PATH:./vendor/bin

WORKDIR /app
EXPOSE 8000

CMD ["php", "artisan", "serve", "--host", "0.0.0.0"]
