FROM bitnami/apache:latest
COPY ./public_html/ /app
# Change Apache to listen on port 8080
RUN sed -i 's/Listen 80/Listen 8080/' /usr/local/apache2/conf/httpd.conf

EXPOSE 8080

RUN chown -R 1001:0 /usr/local/apache2/logs
