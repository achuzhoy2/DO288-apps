FROM quay.io/achuzhoy/fedora27_httpd_ip
EXPOSE 8080
RUN sed -i 's/Listen 80/Listen 8080/g' /etc/httpd/conf/httpd.conf && \
    sed -i "s/IP=/echo 'Hey Elvis'\nIP=/" /var/www/cgi-bin/index.cgi && \
    chgrp 0 -R /var/log/httpd /var/run/httpd && \
    chmod g=u -R /var/run/httpd /var/log/httpd
USER 1001
