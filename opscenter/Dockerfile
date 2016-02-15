FROM kapschtrafficcom/opscenter

RUN apt-get update && apt-get install telnet && mkdir -p /etc/cassandra/

ADD resources/conf /opt/opscenter/conf
ADD resources/cassandra /etc/cassandra/
