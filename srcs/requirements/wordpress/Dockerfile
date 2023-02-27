FROM alpine:3.16.4

RUN apk update
RUN apk add php-fpm

RUN wget https://wordpress.org/latest.tar.gz
RUN tar -xzvf latest.tar.gz
RUN mkdir -p /var/www/html
RUN mv wordpress /var/www/html

COPY ./conf/www.conf /etc/php8/php-fpm.d/www.conf

CMD ["/usr/sbin/php-fpm8", "-F"]
