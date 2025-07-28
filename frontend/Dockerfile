FROM httpd:2.4

COPY ./src/public/ /usr/local/apache2/htdocs/

# Change Apache to use port 8080
RUN sed -i 's/Listen 80/Listen 8080/' /usr/local/apache2/conf/httpd.conf

EXPOSE 8080
