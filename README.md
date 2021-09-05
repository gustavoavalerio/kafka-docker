# kafka-docker
A simple Kafka cluster that runs on Docker

##### Create a topic  
```docker compose exec broker kafka-topics --create --topic test_topic --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1```

##### Describe a topic  
```docker compose exec broker kafka-topics --describe --topic test_topic --bootstrap-server localhost:9092```

##### Send message to topic  
```docker compose exec broker kafka-console-producer --topic test_topic --bootstrap-server localhost:9092```

##### Consume message from topic  
```docker compose exec broker kafka-console-consumer.sh --topic test_topic --from-beginning --bootstrap-server localhost:9092```
