# kafka-producers-consumers-streams

## Start ZooKeeper

```sh

$ bin/zookeeper-server-start.sh config/zookeeper.properties

```

## Start Kafka

```sh

$ bin/kafka-server-start.sh config/server.properties

```

## Create Kafka Topics

```sh

$ bin/kafka-topics.sh --create --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1 --topic STORE_NEW_ORDER

```

## List Kafka Topics

```sh

$ bin/kafka-topics.sh --list --bootstrap-server localhost:9092

```

## Send Message Producers Kafka Topics

```sh

$ bin/kafka-console-producer.sh --broker-list localhost:9092 --topic STORE_NEW_ORDER

```

## Get Message Consumers Kafka Topics

```sh

$ bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic STORE_NEW_ORDER 

$ bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic STORE_NEW_ORDER --from-beginning

```

## Describe Kafka Topics

```sh

$ bin/kafka-topics.sh --bootstrap-server localhost:9092 --describe

```

## Alter Kafka Topics

### The number of partitions must be greater than or equal to the number of consumers within a group

```sh

$ bin/kafka-topics.sh --alter --bootstrap-server localhost:9092 --topic ECOMMERCE_NEW_ORDER --partitions 3

```

## List all Kafka Groups

```sh

bin/kafka-consumer-groups.sh --all-groups --bootstrap-server localhost:9092 --describe

```
