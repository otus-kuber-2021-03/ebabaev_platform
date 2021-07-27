FROM nginx:1.19.3-alpine

RUN apk add --no-cache shadow \
    && usermod -u 1001 nginx \
    && groupmod -g 1001 nginx

WORKDIR /app
RUN echo "server { listen 8000; server_name _; root /app; }"  > /etc/nginx/conf.d/default.conf
RUN chown -R nginx:nginx /var/cache/* && \
    chown -R nginx:nginx /var/run/ && \
    chown -R nginx:nginx /var/log && \
    chown -R nginx:nginx /app 
EXPOSE 8000
USER 1001
