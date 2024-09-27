
# Realtime Data Streaming | End-to-End Data Engineering Project

## Table of Contents
- [Introduction](#introduction)
- [System Architecture](#system-architecture)
- [Key Contributions](#key-contributions)
- [Technologies](#technologies)
- [Deployment Instructions](#deployment-instructions)

## Introduction

This project represents the successful implementation of an end-to-end data engineering pipeline, showcasing real-time data ingestion, processing, and storage. It leverages a modern tech stack including Apache Kafka, Spark, and Cassandra, all orchestrated via Apache Airflow and containerized using Docker. 

The project pulls random user data from the `randomuser.me` API and processes it in real-time. My role was to integrate, deploy, and optimize each stage of the pipeline, ensuring smooth data flow and storage in the Cassandra database.

## System Architecture

![System Architecture](https://github.com/Puravi2018/kafka-spark-data-engineering/blob/main/Data%20engineering%20architecture.png)

The project is structured into several components:

- **Data Source**: Random user data is ingested via the `randomuser.me` API.
- **Apache Airflow**: I implemented Apache Airflow to orchestrate the data pipeline and automate data ingestion into PostgreSQL.
- **Apache Kafka and Zookeeper**: Responsible for real-time data streaming. I set up Kafka and Zookeeper to ensure distributed streaming and fault tolerance.
- **Control Center and Schema Registry**: Configured for monitoring and managing Kafka streams and schemas.
- **Apache Spark**: Deployed Spark for real-time data processing and transformation. This includes configuring the master and worker nodes.
- **Cassandra**: Implemented as the final storage solution for processed data, ensuring efficient query response times and fault-tolerant storage.

## Key Contributions

In this project, I:

- Developed the end-to-end data pipeline, integrating the components for data ingestion, streaming, and storage.
- Implemented **Apache Airflow** to automate the orchestration of the entire workflow, enabling data retrieval and processing at scheduled intervals.
- Configured **Apache Kafka** for real-time data streaming, ensuring low-latency data movement between components.
- Set up **Apache Spark** to perform real-time data transformations, handling the necessary data processing before storage.
- Designed and managed the schema for storing processed data in **Cassandra**, ensuring optimal performance for large-scale data queries.
- Containerized the entire system using **Docker**, making it scalable and easy to deploy across different environments.

## Technologies

- Apache Airflow
- Python
- Apache Kafka
- Apache Zookeeper
- Apache Spark
- Cassandra
- PostgreSQL
- Docker

## Deployment Instructions

To deploy the system:

1. Clone the repository:
    ```bash
    git clone https://github.com/Puravi2018/kafka-spark-data-engineering.git
    ```

2. Navigate to the project directory:
    ```bash
    cd kafka-spark-data-engineering
    ```

3. Use Docker Compose to start the services:
    ```bash
    docker-compose up
    ```

This will initialize all components, including Kafka, Airflow, Spark, and Cassandra, and begin streaming real-time data.
