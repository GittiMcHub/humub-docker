FROM ubuntu:18.04

ENV HUMHUB_VERSION=1.3.6
ENV HUMHUB_WWW_DIR=/var/www

RUN apt-get update \
    && apt-get install -y --no-install-recommends \
    ca-certificates \
    wget \
    imagemagick \
    sqlite \
    exif \
    openssl \
    php7.2 \
    php7.2-fpm \
    php7.2-mbstring \
    php7.2-curl \
    php7.2-cli \
    php7.2-gd \
    php7.2-mysql \
    php7.2-zip \
    php7.2-bz2 \
    php7.2-intl \
    php7.2-json \
    php7.2-sqlite3 \
    php7.2-xml \
    && rm -rf /var/lib/apt/lists/*

RUN wget -q -O /tmp/humhub.tar.gz "https://www.humhub.org/en/download/start?version=$HUMHUB_VERSION&type=tar.gz" \
    && tar xfz /tmp/humhub.tar.gz -C /tmp/ \
    && mkdir -p $HUMHUB_WWW_DIR \
    && mv /tmp/humhub-$HUMHUB_VERSION/* $HUMHUB_WWW_DIR \
    && chown -R www-data:www-data $HUMHUB_WWW_DIR


RUN mkdir -p /run/php

CMD ["/usr/sbin/php-fpm7.2", "-F"]
