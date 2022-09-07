FROM nginx:1-alpine

ENV TZ=UTC

# nginx config file
COPY ./docker/web/*.conf /etc/nginx/conf.d/

WORKDIR /var/www/html