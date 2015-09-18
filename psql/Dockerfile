FROM ubuntu:14.04

RUN apt-get update && apt-get install -y -q postgresql-9.3 postgresql-contrib-9.3 postgresql-9.3-postgis-2.1 libpq-dev sudo

#RUN mkdir /etc/ssl/private-copy; mv /etc/ssl/private/* /etc/ssl/private-copy/; rm -r /etc/ssl/private; mv /etc/ssl/private-copy /etc/ssl/private; chmod -R 0700 /etc/ssl/private; chown -R postgres /etc/ssl/private

#RUN chown postgres:postgres /etc/postgresql/9.3/main/*.conf

#ADD run /usr/local/bin/run

#RUN chmod +x /usr/local/bin/run

#VOLUME ["/var/lib/postgresql"]

EXPOSE 5432

CMD ["/usr/local/bin/run"]

