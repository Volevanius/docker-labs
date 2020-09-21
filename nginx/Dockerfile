# Base image
FROM debian:buster-slim

RUN apt-get update\
&& apt-get install -y nginx\
&& rm /var/log/nginx/access.log && ln -s /dev/stdout /var/log/nginx/access.log\
&& rm /var/log/nginx/error.log && ln -s /dev/stderr /var/log/nginx/error.log\
&& rm -rf /var/lib/apt/lists/*

EXPOSE 80
#CMD nginx -g 'daemon off;'
CMD ["/usr/sbin/nginx", "-g", "daemon off;"]
