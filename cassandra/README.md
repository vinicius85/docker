#### Run cassandra

`docker run -d --name cassandra -p 9042:9042 -p 7199:7199 -p 9160:9160 --env LOCAL_JMX=no -v /var/lib/cassandra:/var/lib/cassandra cassandra`
