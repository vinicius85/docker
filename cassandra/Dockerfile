FROM cassandra:2.2.1

RUN apt-get update  \
	&& apt-get install telnet

COPY ./jmxremote.password /etc/cassandra/jmxremote.password

RUN chmod 400 /etc/cassandra/jmxremote.password

COPY ./jmxremote.password /etc/java-8-openjdk/management/jmxremote.password

ADD resources/conf /etc/cassandra/