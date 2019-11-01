### Setup Ubuntu

- sudo apt update
- sudo apt install default-jdk

### Setup JDK

sudo apt install openjdk-8-jdk
export JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64
echo $JAVA_HOME
export PATH=$PATH:$JAVA_HOME/bin
echo $PATH



## Download Kafka 

```
wget http://www-us.apache.org/dist/kafka/2.2.1/kafka_2.12-2.2.1.tgz
tar xzf kafka_2.12-2.2.1.tgz
mv kafka_2.12-2.2.1 /usr/local/kafka
```

## Step 3 – Start Kafka Server

Kafka uses ZooKeeper, so first, start a ZooKeeper server on your system. You can use the script available with Kafka to get start single-node ZooKeeper instance.

```
cd /usr/local/kafka
bin/zookeeper-server-start.sh config/zookeeper.properties
```
Now start the Kafka server:

```
bin/kafka-server-start.sh config/server.properties
```

...
[2018-03-13 10:47:45,989] INFO Kafka version : 1.0.1 (org.apache.kafka.common.utils.AppInfoParser)
[2018-03-13 10:47:45,995] INFO Kafka commitId : c0518aa65f25317e (org.apache.kafka.common.utils.AppInfoParser)
[2018-03-13 10:47:46,006] INFO [KafkaServer id=0] started (kafka.server.KafkaServer)
.

1- Download Kafka
2- Download Zookeeper
3- Extract Both Kafka and Zookeeper
4- tar -xzf kafka_xxxxxxx.tgz
5- tar -xzf zookeeper_xxx.tgz


goto kafka folder
bin/zookeeper-server-start.sh config/zookeeper.properties



### Setup SSH on Ubuntu VM

1- (Hack) Use Bridge Adapter
The best way to do this is to use a Bridge Adapter in virtualbox. In virtual box go to the settings for your machine->Network->Adapter 1 and select Bridged Adapter. This will make you virtual machine part of your main network.

If you have a dhcp server it should supply an address etc. to the virtual machine which will allow it to communicate with the rest of your systems and vice versa.

Reference
[https://serverfault.com/questions/225155/virtualbox-how-to-set-up-networking-so-both-host-and-guest-can-access-internet]1

# TODO 
- explore NAT and Port forwarding
- kafka cluster
- kafka security
