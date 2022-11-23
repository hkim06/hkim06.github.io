---
title: Database per service
layout: default
parent: Microservices
grand_parent: Software Architecture
---

[Database per service]

Keep each microservice's persisent data private to that service and accessible only via its API. A service's transactions only involve its database. 

Benefits
- Helps ensure that services are loosely coupled. 
- Each service can use the type of database that is best suited to its needs.

Drawbacks
- Implementing business transactions that span multiple services is not straightforward.
- Implementing queries that join data taht is now in multiple databases is challenging
- Complexity of managing multiple SQL and NoSQL databases

Various patterns/solutions for implementing transactions and queries that span services
- Implementing transactions that span services - use the Saga pattern.
- Implementing queries that span services
    - API Composition - the application performs the join rather that the database.
    - Command Query Responsibility Segregation(CQRS) - maintain one or more materalized views that contain data from multiple services. 

[Database per service]: https://microservices.io/patterns/data/database-per-service.html