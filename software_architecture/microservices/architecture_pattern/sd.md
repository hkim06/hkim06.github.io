---
title: Shared database
layout: default
parent: Microservices
grand_parent: Software Architecture
---

[Shared database]

Use a (single) database that is shared by multiple services. Each service freely accesses data owned by other services using local ACID transactions. 

Benefits
- A developer uses familiar and straightforward ACID transactions to enforce data consistency
- A single database is simpler to operate

Drawbacks
- Development time coupling
- Runtime coupling
- Single database might not satisfy the data storage and access requirements of all services.

[Shared database]: https://microservices.io/patterns/data/shared-database.html