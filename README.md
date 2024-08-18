# springboot-kafka-microservices-project
This project demonstrates a microservices architecture using Spring Boot and Kafka. The project consists of three main services: Order Service, Stock Service, and Email Service. Each service communicates with others through Kafka topics to perform specific operations, ensuring a scalable and decoupled system.

![img_2.png](readme-pic%2Fimg_2.png)

## Services
### Base Domains
- This module contains the shared domain classes used across different services.

- Order.java: Represents an order entity.
- OrderEvent.java: Represents an event related to an order.
- BaseDomainsApplication.java: Main application class for base domains.


### Order Service
- Handles order-related operations and publishes order events to Kafka.

- KafkaTopicConfig.java: Configuration for Kafka topics.
- OrderController.java: REST controller for handling order-related requests.
- OrderProducer.java: Produces order events to Kafka.
- OrderServiceApplication.java: Main application class for the order service.
### Stock Service
- Consumes order events from Kafka and handles stock management.
- OrderConsumer.java: Consumes order events from Kafka.
- StockServiceApplication.java: Main application class for the stock service.
 ### Email Service
Handles email notifications related to orders.

## Run the service
```bash
bin/zookeeper-server-start.sh config/zookeeper.properties
bin/kafka-server-start.sh config/server.properties
```

### Order Service

```bash
cd order-service
./mvnw spring-boot:run
```
### Stock Service

```bash
cd stock-service
./mvnw spring-boot:run
```
### Email Service

```bash
cd email-service
./mvnw spring-boot:run
```


## Getting Started
Prerequisites
- Java 17 
- Maven
- Kafka
