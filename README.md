
# Telecommunications Mobile Money Data Streaming with Kafka
This project is a Kafka data engineering solution that can receive real-time data from telecommunications mobile money transactions and process it for analysis. The pipeline is designed to handle high volumes of data and ensure that the data is processed efficiently.

## Setup
To set up the Kafka cluster, follow these steps:

1. Install Kafka on your machine or server.
2. Start the ZooKeeper server using the command: bin/zookeeper-server-start.sh config/zookeeper.properties
3. Start the Kafka broker server using the command: bin/kafka-server-start.sh config/server.properties
Once you have set up the Kafka cluster, you can develop the Kafka producer and consumer.

## Kafka Producer
The Kafka producer can ingest data from telecommunications mobile money transactions and send it to the Kafka cluster. The producer is designed to handle high volumes of data and ensure that the data is sent to the Kafka cluster efficiently.

To run the Kafka producer, navigate to the producer directory and run the following command:

python producer.py

This will start the producer and send the mobile money data to the Kafka cluster.

## Kafka Consumer
The Kafka consumer receives data from the Kafka cluster and processes it for analysis. The consumer is designed to handle high volumes of data and ensure that the data is processed efficiently.

To run the Kafka consumer, navigate to the consumer directory and run the following command:

python consumer.py

This will start the consumer and read the mobile money data from the Kafka cluster.

## Processing Data
Once you have set up the Kafka pipeline, you can process the data for analysis. This may involve cleaning and aggregating the data, performing calculations, and creating visualizations.

To process the data, navigate to the analysis directory and run the following command:

python analysis.py

This will process the mobile money data and create visualizations.

## Testing
To test the solution, use the provided dummy JSON file. The file contains sample data that you can use to ensure that your Kafka pipeline is working correctly.

To produce the sample data to the Kafka cluster, run the following command:

bin/kafka-console-producer.sh --broker-list localhost:9092 --topic mobile-money-transactions < mobile_money_data.json
To consume the sample data from the Kafka cluster, run the following command:

bin/kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic mobile-money-transactions --from-beginning

## Conclusion
This project demonstrates how Kafka can be used to build a robust data engineering solution for real-time data streaming. With the right setup and implementation, you can handle high volumes of data and process it efficiently for analysis
