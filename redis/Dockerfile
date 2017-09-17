FROM redis:latest

ADD redis.conf /etc/redis.conf
WORKDIR /data
ENTRYPOINT ["redis-server", "/etc/redis.conf"]
