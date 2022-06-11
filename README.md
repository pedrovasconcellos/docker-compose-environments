# Docker compose environments
Docker compose environments

#### Install Kafka (to run the commands below)
```sh
brew install kafka
```
OR
```sh
sudo apt-get install kafka
```



#### Create Topic
```sh
kafka-topics --bootstrap-server localhost:9092 --topic first_topic --create --partitions 3 --replication-factor 1
```

#### Create Message in Broker
```sh
kafka-console-producer --bootstrap-server localhost:9092 --topic first_topic
```

#### Listening Message in Broker
```sh
kafka-console-consumer --bootstrap-server localhost:9092 --topic first_topic --group firsttopic
```

#### Show info of all Topics
```sh
watch kafka-consumer-groups --all-groups --bootstrap-server localhost:9092 --all-topics -describe
```
