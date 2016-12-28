FROM ubuntu:14.04

RUN apt-get update && apt-get install -y python-pip supervisor openssh-server && rm -rf /var/lib/apt/lists/*

RUN pip install shadowsocks

COPY supervisord.conf /etc/supervisor/
COPY supervisord_shadowsocks.conf /etc/supervisor/conf.d/
COPY shadowsocks.json /etc/

EXPOSE 2525

ENTRYPOINT /usr/bin/supervisord
