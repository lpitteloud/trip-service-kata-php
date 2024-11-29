FROM php:8.4-cli-alpine

ENV COMPOSER_ALLOW_SUPERUSER=1

RUN apk update && apk add --no-cache \
    bash \
    zlib \
    zlib-dev \
    libzip \
    libzip-dev \
    unzip

RUN docker-php-ext-install zip

COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

RUN composer self-update

WORKDIR /app

COPY composer.json composer.lock* ./

RUN composer install --no-dev --no-interaction --optimize-autoloader

COPY . .

CMD ["tail", "-f", "/dev/null"]