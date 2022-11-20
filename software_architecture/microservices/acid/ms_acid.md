---
title: ACID 
layout: default
parent: Microservices
grand_parent: Software Architecture
---

ACID is an an acronym outlining the key properties of database transactions. 

    Atomicity    
        Ensures that all operations completed within the transaction either all complete or all fail. 

    Comsistency
        When changes are made to our database. We ensure it is left in a valid, consistent state. 

    Isolation
        Allows multiple transactions to operate at the same time without interfering.

    Durability
        Makes sure that once a transaction has been completed, the data won't get lost by system failures. 

In microservices, data ownership is decentralized as every service is autonomous and  has its own private data store relevant to its functionality.

Therefore, you can't use ACID transactions for transactions outside a single service. 

