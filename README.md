# KAFKA


https://grokonez.com/spring-framework/spring-boot/start-spring-apache-kafka-application-springboot

https://grokonez.com/java-integration/start-apache-kafka

https://www.loginradius.com/blog/async/quick-kafka-installation/

C:\kafka_2.12-0.10.2.1(In my PC)

According to this link I modify these two file.
modify the config/zookeeper.properties file      dataDir=C:\kafka\zookeeper
modify the config/server.properties file           log.dirs=C:\kafka\kafka-logs

Change Environment variable (otherwise ‘wpic’ is not recognized as internal or external command bhan6)
Variable name: Path
Variable value: C:\Windows\System32\wbem;%SystemRoot%\System32\;SystemRoot%;%PATH%;

Commands
 Start a ZooKeeper:
C:\kafka_2.12-0.10.2.1>.\bin\windows\zookeeper-server-start.bat .\config\zookeeper.properties
 
-> Logs:
[2017-06-06 17:59:52,636] INFO Reading configuration from: .\config\zookeeper.properties
...
– Start the Apache Kafka server:
C:\kafka_2.12-0.10.2.1>.\bin\windows\kafka-server-start.bat .\config\server.properties
 
-> Logs:
[2017-06-06 18:06:53,365] INFO starting (kafka.server.KafkaServer)
[2017-06-06 18:06:53,367] INFO Connecting to zookeeper on localhost:2181 (kafka.server.KafkaServer)
[2017-06-06 18:06:53,379] INFO Starting ZkClient event thread. (org.I0Itec.zkclient.ZkEventThread)
...
-Run Spring boot project

Make a producer request: http://localhost:8080/jsa/kafka/producer?data=Hello World

Make a consumer request: http://localhost:8080/jsa/kafka/consumer

http://localhost:8080/jsa/kafka/producer?data=praja

http://localhost:8080/jsa/kafka/consumer
