FROM ubuntu

ADD ./Deploy-Nami.sh /tmp
RUN /bin/sh /tmp/Deploy-Nami.sh
CMD service php7.0-fpm start && nginx -g "daemon off;"

EXPOSE 80

