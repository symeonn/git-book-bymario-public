# Architecture

## Good architecture is about deferring decisions about UI, DB, service layer, frameworks, web servers etc.&#x20;

## Keep options open for as long as possible

## It maximizes the number of decisions NOT made&#x20;

Architecture is about whole high level concepts and low level implementation details

programmers are architectures

Architecture is not about tools and building materials, it is about **usage, how the system is being used,  screams use cases, not delivery mechanism or tools used to build that system**

Arch of program screams the intention of that program like architecture of church screams church intention

Use cases not coupled to delivery mechanisms (UI, DB) - design the structure that decouples you from them and make them irrelevant

separating those allow business people to measure the costs and ration between cost of different aspects of the system - cost vs value analysis

### Use cases

when desinging system think of USE CASES, what system do (not how to do)

models are not business objects

delivery mechanisms are the details (not abstractions - see the dependency directions) these should be able to be substituted at any point of time

we use words and conccepts that do not suggest delivery mechanisms

use cases are the formal description how user interacts with the system in order to achieve a specific goal (for example "happy path"), there is albo exception path

delivery independent architecture is delivery independent use cases

use case might be considered as algorithm that takes input data and generates output data

### Example:

consider UI and backend. UI is a plugin. Backend is exposing endpoints and do not know anything about who is going to read from it. UI needs to know about backend, know what are the endpoints and how requests and responses looks like. \
This approach can be applied to every components on every level (server level too?) and it is easy to understand.





