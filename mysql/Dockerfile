FROM mysql:latest

ENV TZ PRC

RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone \
    && chown -R mysql:root /var/lib/mysql/

CMD ["mysqld"]

EXPOSE 3306
