# KAFKA

## What is Kafka:

### Kafka definition:

Kafka is a log messaging system. Kafka has the following characteristics:

* Distributed Storage

* High throughput

* Load rebalancing

* Messaging-oriented system

* Event driven architecture


### Kafka usage:

* The purpose of Kafka is to ingest data. 

* Data Ingestion: Kafka can ingest data in batch and also streaming mode. Since It's a messaging system, the size of data (message, log) should be medium and small. Because of this, the best practice for Kafka support ingest data by streaming.

## How Kafka generally work:

### Terms:

**Message**: data

**Consume**: read data from kafka

**Produce**: write data into kafka

**Topic**: category of data 

**subcribe**: Assigning consumer to a Topic

### Components:

Kafka architect consists of 3 main components:

* Broker:

	* A server to store and serve message   

	* `kafkaServer`, `kafkaStorage`

* Producer: 

	*  A client connected to broker and produce message
	
	* `kafkaClient`

* Consumer:

	* A client connected to brokder and consume message

	* `kafkaClient`

### Kafka Mechanism:

Messages in Kafka are organized into `Topic`. Data refer to the same subject should be in the same 'Topic'.

1. Brokers publish a new Topic

2. Producers produce message to a specific Topic

3. Consumer subcribe to a specific topic

4. Consumer consume messages
