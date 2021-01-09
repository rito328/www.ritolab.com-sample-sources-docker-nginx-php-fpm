FROM php:8.0-fpm-alpine

# update package list
RUN apk update

# add user
RUN addgroup -S nginx && adduser -S nginx -G nginx

# install setting
RUN cp /usr/local/etc/php/php.ini-production /usr/local/etc/php/php.ini

# settings
COPY settings/zzz-docker.conf /usr/local/etc/php-fpm.d/zzz-docker.conf
COPY settings/php.ini /usr/local/etc/php/conf.d/php.ini

# unix socket
RUN mkdir /var/run/php-fpm
VOLUME ["/var/run/php-fpm"]

# app sources
COPY src /usr/share/nginx/html
