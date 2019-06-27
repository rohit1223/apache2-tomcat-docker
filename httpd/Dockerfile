FROM ubuntu:latest

RUN apt-get update && apt-get install -y --no-install-recommends apache2 libapache2-mod-jk

ADD apache2.conf /etc/apache2/apache2.conf

ADD 000-default.conf /etc/apache2/sites-enabled/000-default.conf

#ADD default-ssl.conf /etc/apache2/sites-enabled/default-ssl.conf
#ADD localhost.crt /etc/ssl/certs/localhost.crt
#ADD localhost.key /etc/ssl/private/localhost.key
#RUN a2enmod rewrite
#RUN a2enmod ssl
#RUN a2enmod headers
#RUN a2ensite default-ssl

ADD worker.properties /etc/libapache2-mod-jk/workers.properties

ADD jk.conf /etc/apache2/mods-available/jk.conf

ADD static /var/www/html/

VOLUME ["/var/log/apache2"]

EXPOSE 80 443

CMD ["apachectl", "-k", "restart", "-DFOREGROUND"]
