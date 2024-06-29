FROM php:7.4.4-fpm
RUN docker-php-ext-install sockets
RUN apt-get update && apt-get install -y cron
RUN curl -sS https://getcomposer.org/installer -o composer-setup.php
RUN php composer-setup.php --install-dir=/usr/local/bin --filename=composer
RUN rm -rf composer-setup.php
COPY ./entrypoint.sh /
RUN chmod 755 /entrypoint.sh
ENTRYPOINT /entrypoint.sh
