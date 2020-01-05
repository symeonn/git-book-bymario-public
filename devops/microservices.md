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
* 
No one starts with microservices \(there is no need\), but after some point there is need to move to microservices

It is good to start with monolith, as long as you can get away with disadvantages.



