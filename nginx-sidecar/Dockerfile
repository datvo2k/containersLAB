FROM nginx:1.27-alpine-slim

COPY nginx.conf.template /etc/nginx/nginx.conf.template
COPY start.sh /usr/bin/start.sh
RUN chmod a+x /usr/bin/start.sh

RUN chown -R nginx:nginx /etc/nginx/nginx.conf.template /usr/bin/start.sh /var/cache/nginx /var/log/nginx /etc/nginx/conf.d

RUN touch /etc/nginx/nginx.conf && \
    chown -R nginx:nginx /etc/nginx/nginx.conf

RUN touch /var/run/nginx.pid && \
RUN touch /etc/nginx/nginx.conf && chown -R nginx:nginx /etc/nginx/nginx.conf && \
    touch /var/run/nginx.pid && chown -R nginx:nginx /var/run/nginx.pid

USER nginx
CMD ["/usr/bin/start.sh"]