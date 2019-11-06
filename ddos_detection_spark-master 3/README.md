# ddos_detection_spark

# DDOS Attacks Detector
This is a simple real-time DDOS attack detector application based on Kafka messaging system and Spark Streaming. 
In this application Apache access log data is ingested into Kafka broker using producer API and the detector application uses the streaming data to perform real-time analysis to find the DDOS attacks.
Current state: Read log file from local and use producer API to push to Kafka topic and then read from kafka topic using consumer API and dump output into Local Directory
## Prerequisite:
* kafka_2.2.0
* spark-streaming-kafka-0-10_2.11
* spark-core_2.11
* spark-streaming_2.11
* scala_2.11
* Java_1.8
## Installation:
* Cloudera Quickstart VM
* JDK 8u201
* Kafka_2.2.0
* Zookeeper
* Eclipse Oxygen (4.7)
* Scala Eclipse IDE

## Apache log message sample
```
200.4.91.190 - - [25/May/2015:23:11:15 +0000] "GET / HTTP/1.0" 200 3557 "-" "Mozilla/4.0 (compatible; MSIE 6.0; Windows NT 5.1; SV1)"

```
## Steps:
1.	Create         
2.	Start Kafka topic and start Kafka Server ,I have used open source confluencekafka           
3.	Run the Detector Application producer API
4.	Start the consumer API             
5.	Save the output in a CSv file in local

## Notes:

1.	The application is run on the local machine, but this solution is scalable and can be run on multiple clusters.
2.	I can include multiple use cases but limiting to single use case case for now

