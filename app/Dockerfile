FROM docker.io/alpine:latest

RUN apk update && apk add --update lighttpd \
        && rm -rf /var/cache/apk/*

COPY ./conf/* /etc/lighttpd/

COPY ./html/* /var/www/html/

EXPOSE 80

CMD ["lighttpd","-D","-f","/etc/lighttpd/lighttpd.conf"]
