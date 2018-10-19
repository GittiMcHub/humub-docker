FROM alpine

ENV HUMHUB_VERSION=1.3.6

RUN apk add --no-cache nginx \
      wget \
      gettext \
      libintl

RUN wget -q -O /tmp/humhub.tar.gz "https://www.humhub.org/en/download/start?version=$HUMHUB_VERSION&type=tar.gz"
RUN tar xfz /tmp/humhub.tar.gz -C /tmp/
RUN mv /tmp/humhub-$HUMHUB_VERSION/* /var/www \
    && chown -R nginx:nginx /var/www

RUN mkdir /run/nginx/
