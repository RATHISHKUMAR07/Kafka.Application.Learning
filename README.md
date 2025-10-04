# Kafka Application Learning

This repository demonstrates the implementation of Apache Kafka in a Spring Boot application, focusing on event-driven architecture, message production and consumption, and integration testing with embedded Kafka.

## Table of Contents

* [Project Overview](#project-overview)
* [Technologies Used](#technologies-used)
* [Setup and Installation](#setup-and-installation)
* [Kafka Topics](#kafka-topics)
* [Running the Application](#running-the-application)
* [Testing](#testing)
* [Contributing](#contributing)
* [License](#license)

## Project Overview

This project serves as a learning resource for integrating Apache Kafka with Spring Boot applications. It covers:

* Creating and configuring Kafka producers and consumers.
* Setting up Kafka listeners and handlers.
* Implementing retry mechanisms and dead-letter topics.
* Performing integration tests with embedded Kafka.
* Utilizing WireMock for external service simulation.

## Technologies Used

* **Spring Boot 3.5.6**
* **Spring Kafka 3.3.10**
* **Apache Kafka 3.9.1**
* **WireMock** for HTTP service stubbing
* **JUnit 5** for testing
* **Awaitility** for asynchronous test synchronization

## Setup and Installation

### Prerequisites

* Java 17 or higher
* Apache Kafka (for local development)
* Maven 3.8+

### Clone the Repository

```bash
git clone https://github.com/RATHISHKUMAR07/Kafka.Application.Learning.git
cd Kafka.Application.Learning
```

### Build the Project

```bash
mvn clean install
```

### Run the Application

```bash
mvn spring-boot:run
```

By default, the application will connect to a locally running Kafka instance.

## Kafka Topics

The application interacts with the following Kafka topics:

* `order.created`
* `order.dispatched`
* `dispatch.tracking`

These topics are used to simulate order processing workflows, including dispatch preparation, order dispatch, and completion events.

## Running the Application

To start the application, ensure that your Kafka broker is running locally. You can use the following command to start a Kafka broker:

```bash
kafka-server-start.sh config/server.properties
```

Once Kafka is running, execute the Spring Boot application as mentioned in the "Run the Application" section.

## Testing

The project includes integration tests that use embedded Kafka and WireMock for simulating external HTTP services. To run the tests, use the following command:

```bash
mvn test
```

The tests cover various scenarios, including:

* Successful order dispatch flow.
* Handling of non-retryable exceptions.
* Retry logic with eventual success.

## Contributing

Contributions are welcome! Please fork the repository, create a new branch, and submit a pull request with your proposed changes.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
