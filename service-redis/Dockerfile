FROM debian:11

RUN apt-get update && apt-get install -y python3 procps coreutils less telnet netcat-openbsd iputils-ping redis
RUN apt-get update && apt-get install -y vim

WORKDIR /home/redis

CMD [ "redis-server", "/app/config/redis.conf"]
