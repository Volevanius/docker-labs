# Base image
FROM debian:buster-slim

RUN apt-get update
RUN apt-get install -y nginx
RUN rm /var/log/nginx/access.log && ln -s /dev/stdout /var/log/nginx/access.log
RUN rm /var/log/nginx/error.log && ln -s /dev/stderr /var/log/nginx/error.log

ADD ./html.tar /var/www/
ADD http://example.com/index.html /var/www/html/example.html

EXPOSE 80
#CMD nginx -g 'daemon off;'
CMD ["/usr/sbin/nginx", "-g", "daemon off;"]
