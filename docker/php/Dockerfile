FROM php:7.4.1-fpm

# install composer
RUN cd /usr/bin && curl -s http://getcomposer.org/installer | php && ln -s /usr/bin/composer.phar /usr/bin/composer
RUN apt-get update \
  && apt-get install -y \
  git \
  zip \
  unzip \
  vim

# install nodejs
RUN curl -sL https://deb.nodesource.com/setup_10.x | bash -
RUN apt-get install -y nodejs

RUN apt-get update \
  && apt-get install -y libpq-dev \
  && docker-php-ext-install pdo_mysql pdo_pgsql


WORKDIR /var/www/html
