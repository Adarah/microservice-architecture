# 2. Use a microservice architecture

Date: 2020-11-07

## Status

Accepted

## Context

We want different "modules" in the application to be decoupled from each other, and for them to be able to use different technological stacks if required.

## Decision

We will use microservices to encapsulate domains to their respective mini-applications. Each microservice should own it's own database and domain.


## Consequences

- Usage of microservices introduces some extra complexity when reasoning about the program as a whole, but facilitates the understanding of a single service as a unit
- A polyglot stack for each microservice might make it harder to jump from project to project
- Microservices introduce difficulties when it comes to data consistency across services, requiring the usage of patterns such as Sagas to maintain isolation levels
- Microservices allow for more rapid development and allows services to evolve independently
