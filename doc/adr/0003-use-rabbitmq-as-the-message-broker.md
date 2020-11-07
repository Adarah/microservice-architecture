# 3. Use RabbitMQ as the message broker

Date: 2020-11-07

## Status

Accepted

## Context

When writing microservices, it is necessary to use asynchronous protocols to avoid reducing the availability of services that depend on other services.


## Decision

We will use RabbitMQ as our message broker. Kafka would also work, but introduces a lot of additional complexity to the project. While Kafka scales better and allows for cool features such as replaying the messages in a timeframe, such performance needs are not necessary as of now.

## Consequences

Each service will no longer have its availability reduced by the downtime of other services.
Using a message broker allows for services to be unaware of other existing services, they only have to know about the channel the other services will listen on.
RabbitMQ in particular is a battle-tested and well known message broker, and seems to be easier to operator than Apache Kafka.
