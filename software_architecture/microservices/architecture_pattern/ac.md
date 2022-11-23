---
title: API Composition
layout: default
parent: Microservices
grand_parent: Software Architecture
---

[API Composition]

Implement q query by defining an API Composer, which invoking the services that own the data and performs an in-memory join of the results.

Benefits
- It is a simple way to query data in a microservice architecture

Drawbacks
- Some queries would result in inefficient, in-memory joins of large datasets.

[API Composition]: https://microservices.io/patterns/data/api-composition.html