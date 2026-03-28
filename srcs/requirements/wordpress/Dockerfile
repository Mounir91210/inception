FROM debian:bookworm
RUN apt-get update -y  && apt-get upgrade -y
RUN apt-get -y install wget
RUN apt-get install -y php\
    php-fpm\
    php-mysql\
    mariadb-client \
    curl

RUN wget https://fr.wordpress.org/wordpress-6.0-fr_FR.tar.gz -P /var/www
RUN cd /var/www && tar -xzf wordpress-6.0-fr_FR.tar.gz && rm wordpress-6.0-fr_FR.tar.gz
RUN	chown -R www-data:www-data /var/www/wordpress
COPY ./conf/www.conf /etc/php/8.2/fpm/pool.d/www.conf
COPY ./tools/wordpress_config.sh /

WORKDIR /var/www/wordpress

ENTRYPOINT ["bash", "/wordpress_config.sh"]