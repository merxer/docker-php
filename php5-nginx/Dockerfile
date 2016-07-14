FROM ubuntu:14.04.4
RUN apt-get update \
    && apt-get install -y nginx \
    && apt-get install -y php5-fpm  \
    && apt-get install -y curl

COPY src/php.ini /etc/php5/fpm/
COPY src/index.php /usr/share/nginx/html/
COPY src/nginx/default /etc/nginx/sites-available/
RUN echo "daemon off;" >> /etc/nginx/nginx.conf

CMD  service php5-fpm restart  && nginx 

EXPOSE 80
