FROM redis:latest

RUN mkdir -p /usr/local/etc/redis
COPY redis.conf /usr/local/etc/redis/redis.conf

VOLUME /data_php

EXPOSE 6379

CMD ["redis-server", "/usr/local/etc/redis/redis.conf"]
