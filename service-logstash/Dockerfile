FROM debian:11

RUN apt-get update && apt-get install -y procps coreutils less telnet netcat-openbsd iputils-ping apt-transport-https wget vim
RUN apt-get update && apt-get install -y gpg
RUN echo "deb [signed-by=/usr/share/keyrings/elasticsearch-keyring.gpg] https://artifacts.elastic.co/packages/7.x/apt stable main" | tee /etc/apt/sources.list.d/elastic-8.x.list
RUN wget -qO - https://artifacts.elastic.co/GPG-KEY-elasticsearch | gpg --dearmor -o /usr/share/keyrings/elasticsearch-keyring.gpg \
        && apt-get update && apt-get install -y logstash=1:7.17.18-1

WORKDIR /home/logstash

CMD [ "/usr/share/logstash/bin/logstash", "--debug", "--path.settings", "/app/config/" ]
