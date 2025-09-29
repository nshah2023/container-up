FROM httpd:2.4

COPY ./public_html/ /usr/local/apache2/htdocs/

# Change listen port (since non-root can't bind 80)
RUN sed -i 's/Listen 80/Listen 8080/' /usr/local/apache2/conf/httpd.conf \
    && echo "ServerName localhost" >> /usr/local/apache2/conf/httpd.conf \
    && sed -i 's#PidFile logs/httpd.pid#PidFile /tmp/httpd.pid#' /usr/local/apache2/conf/httpd.conf

EXPOSE 8080
RUN chmod -R 777 /usr/local/apache2/logs

