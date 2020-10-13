SF Crime Statistics with Spark Streaming - Udacity Project
Introduction
In this project, you will be provided with a real-world dataset, extracted from Kaggle, on San Francisco crime incidents, and you will provide statistical analyses of the data using Apache Spark Structured Streaming. You will draw on the skills and knowledge you've learned in this course to create a Kafka server to produce data, and ingest data through Spark Structured Streaming.

How to use the application

1. Zookeeper:
   /usr/bin/zookeeper-server-start config/zookeeper.properties

2. Kafka server:
   /usr/bin/kafka-server-start config/server.properties

3. Insert data into topic:
   python kafka_server.py

4. Kafka consumer:
   kafka-console-consumer --topic "udacity.project.calls" --from-beginning --bootstrap-server localhost:9092

5. Run Spark job:
   spark-submit --packages org.apache.spark:spark-sql-kafka-0-10_2.11:2.3.4 --master local[*] data_stream.py