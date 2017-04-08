FROM php:7.0

MAINTAINER CS "cs17899219@gmail.com"

RUN apt-get update && apt-get install -y zip unzip git libssl-dev libmagickwand-dev && apt-get clean

RUN curl --location --output /usr/local/bin/phpunit https://phar.phpunit.de/phpunit.phar && chmod +x /usr/local/bin/phpunit

RUN php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" && \
    php composer-setup.php --install-dir=/usr/local/bin && \
    php -r "unlink('composer-setup.php');" && \
    mv /usr/local/bin/composer.phar /usr/local/bin/composer && \
    chmod +x /usr/local/bin/composer

RUN pecl channel-update pecl.php.net && \
 pecl install redis && \
 pecl install mongodb && \
 pecl install imagick && \
 docker-php-ext-enable redis mongodb imagick

RUN docker-php-ext-install pdo_mysql
