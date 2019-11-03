# Num: Config

Simple Spring Cloud Config server for 'Num' solution.

## Application details

To start Kafka:

    $ ./bin/zookeeper-start-server.sh ./config/server.properties &
    $ ./bin/kafka-start-server.sh ./config/server.properties &
    $ ./bin/kafka-console-consumer --bootstrap-server localhost:9092 --topic test --from-beginning

To run Zipkin with Kafka:

    $ export KAFKA_BOOTSTRAP_SERVERS=fangorn:9092
    $ java -jar zipkin.jar

To run ELK stack with Kafka:

    $ ./logstask/bin/logstash.sh -f <num-config path>/src/main/resources/logstash-kafka/logstash-kafka.conf
    $ ./elasticsearch/bin/elasticsearch
    $ ./kibana/bin/kibana

