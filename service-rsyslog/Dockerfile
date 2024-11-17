FROM debian:11

RUN apt-get update && apt-get install -y python3 procps coreutils less telnet netcat-openbsd iputils-ping rsyslog vim bsdutils
RUN apt-get install -y rsyslog-hiredis redis-server

WORKDIR /home/rsyslog

CMD [ "rsyslogd", "-n", "-d", "-f", "/app/config/rsyslog.conf" ]
