FROM kapschtrafficcom/datastax-agent

RUN apt-get update \
	&& apt-get install telnet \
	&& mkdir -p /etc/cassandra/

COPY resources/conf /opt/agent/conf
COPY resources/cassandra /etc/cassandra