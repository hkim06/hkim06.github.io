---
title: Saga
layout: default
parent: Microservices
grand_parent: Software Architecture
---

[Saga]

Implement each business transaction that spans multiple services is a saga. A saga is a sequence of local transactions. Each local transaction updates the database and publishes a message or event to trigger the next local transaction in the saga. If a local transaction fails because it violates a business rule then the saga executes a series of compensating transactions that undo the changes that were made by the preceding local transactions. 

Benefits
- It enables an application to maintain data consistency across multiple services without using distributed transactions

Drawbacks
- The programming model is more complex. 

Issues to address
- In order to be reliable, a service must atomically update its database and publish a message/event. 
- A client that initiates the saga, which an asynchronous flow, using a synchronous request needs to be able to determine its outcome. There are several options, each with different trade-offs: 
    - The service sends back a response once the saga completes. 
    - The service sends back a response after initiating the saga and the client periodically polls to determin the outcome
    - The service sends back a response after initiating the saga, and then sends an event to the client once the saga completes. 

[Saga]: https://microservices.io/patterns/data/saga.html