### Setup Ubuntu

- sudo apt update
- sudo apt install default-jdk


## Download Kafka 

wget http://www-us.apache.org/dist/kafka/2.2.1/kafka_2.12-2.2.1.tgz
tar xzf kafka_2.12-2.2.1.tgz
mv kafka_2.12-2.2.1 /usr/local/kafka

## Step 3 – Start Kafka Server

Kafka uses ZooKeeper, so first, start a ZooKeeper server on your system. You can use the script available with Kafka to get start single-node ZooKeeper instance.

cd /usr/local/kafka
bin/zookeeper-server-start.sh config/zookeeper.properties
Now start the Kafka server:

bin/kafka-server-start.sh config/server.properties

...
[2018-03-13 10:47:45,989] INFO Kafka version : 1.0.1 (org.apache.kafka.common.utils.AppInfoParser)
[2018-03-13 10:47:45,995] INFO Kafka commitId : c0518aa65f25317e (org.apache.kafka.common.utils.AppInfoParser)
[2018-03-13 10:47:46,006] INFO [KafkaServer id=0] started (kafka.server.KafkaServer)
