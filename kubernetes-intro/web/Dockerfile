FROM nginx:alpine

ENV NGINX_USER=1001
ENV NGINX_PORT=8000

COPY nginx.conf /etc/nginx/nginx.conf \
     /app/homework.html /app/homework.html

RUN touch /var/run/nginx.pid && \
  chown -R ${NGINX_USER} /var/run/nginx.pid && \
  chown -R ${NGINX_USER} /var/cache/nginx

EXPOSE ${NGINX_PORT}

USER ${NGINX_USER}