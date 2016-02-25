#### Run Cassandra

`docker run -d --name cassandra -p 9042:9042 -p 7199:7199 -p 9160:9160  -v /var/lib/cassandra:/var/lib/cassandra cassandra`

#### Run Opscenter

`docker run -d --name opscenter -p 8888:8888 -p 61620:61620 opscenter`

#### Run DataStax Agent

`docker run -d --name agent --env DATASTAX_AGENT_OPSCENTER_HOST=$OPSCENTER_IP --env DATASTAX_AGENT_OPSCENTER_PORT=61620 -v /var/lib/cassandra:/var/lib/cassandra agent`

#### TODOs
- DataStax agent cannot retrieve data directories info (commitlog, data, caches)