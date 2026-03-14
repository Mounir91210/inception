FROM debian:bookworm
RUN apt-get update -y && apt-get upgrade -y
RUN apt-get install mariadb-server -y
COPY conf/default.cnf	/etc/mysql/mariadb.conf.d/50-server.cnf
COPY tools/init-db.sh /init-db.sh
RUN chmod +x /init-db.sh
CMD ["/init-db.sh"]