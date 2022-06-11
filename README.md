# docker-compose-environments
Docker compose environments

### Install Kafka
brew install kafka


### Create Topic
kafka-topics --bootstrap-server localhost:9092 --topic first_topic --create --partitions 3 --replication-factor 1

### Create Message in Broker
kafka-console-producer --bootstrap-server localhost:9092 --topic first_topic

### Listening Message in Broker
kafka-console-consumer --bootstrap-server localhost:9092 --topic first_topic --group firsttopic

### Show info of all Topics
watch kafka-consumer-groups --all-groups --bootstrap-server localhost:9092 --all-topics -describe
