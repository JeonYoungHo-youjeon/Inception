FROM alpine:3.16.4

RUN apk update
RUN apk add php-fpm

RUN mkdir -p /var/www/html

COPY ./tools/phpinfo.php /var/www/html/phpinfo.php
# TODO: 설정파일 복사 필요
EXPOSE 9000

CMD ["/usr/sbin/php-fpm8", "-F"]
