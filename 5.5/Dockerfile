# docker-gitlab-ci-runner-php

FROM php:5.5
MAINTAINER  Leo "leo.on.the.earth@gmail.com"

# Install composer
RUN cd /tmp && \
mkdir /root/.composer && \
curl -sS https://getcomposer.org/installer | php && \
mv composer.phar /usr/local/bin/composer

VOLUME ["/root/.composer"]
