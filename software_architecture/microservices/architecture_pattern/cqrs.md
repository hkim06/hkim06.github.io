---
title: Command Query Responsibility Segregation (CQRS)
layout: default
parent: Microservices
grand_parent: Software Architecture
---

[CQRS]

Define a view database, which is a read-only replica that is designed to support that query. The application keeps the replica up to data by subscribing to Domain events published by the service that own the data. 

Benefits
- Supports multiple denormalized views that are scalable and performant
- Improved separation of concerns 
- Necessary in an event sourced architecture

Drawbacks
- Increased complexity
- Potential code duplication
- Replication lag/eventually consistent views

[CQRS]: https://microservices.io/patterns/data/cqrs.html