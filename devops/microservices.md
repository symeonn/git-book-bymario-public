# microservices

### Goals

* stability
* feature velocity - team move rapidly and **independently**
* resilient (sprężysty) - components are isolated

### Characteristics

* single purpose
* simple
* well defined interface
* modular and independent
* isolated persistence

### Extracting DB

decouple apps from DB

* build service to represent domain in DB (for one or more tables)
* make apps use this service instead of DB directly
* extract appropriate table(s) from monolith DB to service DB

### 3 (or 4) tiers of application

* presentation layer - UI
* application layer - stateless business logic
* persistence - DB of any kind
* **events - communication mechanism for microservice elements**

## **Techniques for DB**

### **Shared Data**

#### **Problem: **where data that is used by several parts of application should be put

Single system (service) of record - entity should have only one home, one service, all other services/apps read from this service for data, every other copy is read-only cache

**Synchronous lookups **- services asks specific service on-demand, in real time (may end up in lots of requests)

**asynchronous events + local cache **- specific service sends update event when entity was changed

### Joins

#### Problem: how to join tables from different services)

**Join in client **- first get date from one service and then, using that data, query second service (may face performance issues)

**Materialized view **- create another service that keeps data from few services, it listens events directed to these services, has it's own DB (used by noSQL, analytic systems, search engines)

### Transactions

#### Problem: how to do atomic with several entities - it is hard/impossible

**do not use distributed transactions** - scalability killer

#### Saga - model the transaction as state machine of atomic events

transaction A -> event -> transaction B -> event -> transaction C&#x20;

rollback

transaction C -> event -> transaction B -> event -> transaction A&#x20;

Used by:\
payment processes, expense approval, any multi-step **workflow **

example of workflow:\
commit, tests, review, UAT, deploy (imagine simple rollback)

Events issues:\
not delivered\
delivered twice

Make event system "at-least-once-delivered-system" - Idempotence - property of operations that can be applied multiple times without changing the result

No one starts with microservices (there is no need), but after some point there is need to move to microservices

It is good to start with monolith, as long as you can get away with disadvantages.

microservice does not extract or divide apps, **it creates new services **(nomen omen)

ELT can be one of the services

## SOURCES

{% embed url="https://www.infoq.com/presentations/microservices-managing-data/" %}

## TODO

check: CRDT - conflict replicated data types

how to cope with order of events

