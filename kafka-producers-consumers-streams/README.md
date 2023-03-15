# kafka-producers-consumers-streams

## Start ZooKeeper

```sh

bin/zookeeper-server-start.sh config/zookeeper.properties

```

## Start Kafka

```sh

bin/kafka-server-start.sh config/server.properties

```

## Create Kafka Topics

```sh

bin/kafka-topics.sh --create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1 --topic STORE_NEW_ORDER

```

## List Kafka Topics

```sh

bin/kafka-topics.sh --list --bootstrap-server localhost:9092

```

## Send Message Producers Kafka Topics

```sh

bin/kafka-console-producer.sh --broker-list localhost:9092 --topic STORE_NEW_ORDER

```

## Get Message Consumers Kafka Topics

```sh

bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic STORE_NEW_ORDER 

bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic STORE_NEW_ORDER --from-beginning

```

