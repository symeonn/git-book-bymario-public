# microservices

### Goals

* stability
* feature velocity - team move rapidly and **independently**
* resilient \(sprężysty\) - components are isolated

### Characteristics

* single purpose
* simple
* well defined interface
* modular and independent
* isolated persistence

### Extracting DB

decouple apps from DB

* build service to represent domain in DB \(for one or more tables\)
* make apps use this service instead of DB directly
* extract appropriate table\(s\) from monolith DB to service DB

### 3 \(or 4\) tiers of application

* presentation layer - UI
* application layer - stateless business logic
* persistence - DB of any kind
* **events - communication mechanism for microservice elements**

##  **Techniques for DB**

No one starts with microservices \(there is no need\), but after some point there is need to move to microservices

It is good to start with monolith, as long as you can get away with disadvantages.

microservice does not extract or divide apps, **it creates new services** \(nomen omen\)

ELT can be one of the services

## SOURCES

{% embed url="https://www.infoq.com/presentations/microservices-managing-data/" %}



