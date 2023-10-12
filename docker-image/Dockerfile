FROM amazonlinux

RUN yum -y update \
    && yum -y install httpd \
    php \
    && yum -y clean all \
    && rm -rf /var/cache \
    && mkdir /run/php-fpm

COPY ./index.php /var/www/html/index.php

CMD /usr/sbin/php-fpm && /usr/sbin/httpd -D FOREGROUND

EXPOSE 80
