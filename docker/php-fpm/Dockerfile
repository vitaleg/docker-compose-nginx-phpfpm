FROM php:7.4.4-fpm
RUN docker-php-ext-install sockets
RUN apt-get update && apt-get install -y cron
COPY ./docker/php-fpm/entrypoint.sh /
ENTRYPOINT /entrypoint.sh
