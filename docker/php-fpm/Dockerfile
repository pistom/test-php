FROM php:7.4-fpm
RUN apt-get update && apt-get install -y \
  zip
RUN php -r "readfile('http://getcomposer.org/installer');" | php -- --install-dir=/usr/bin/ --filename=composer
RUN docker-php-ext-install pdo pdo_mysql 
WORKDIR /var/www
CMD composer install ; php-fpm
EXPOSE 9000