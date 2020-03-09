# SOLID

Design principles encourage us to create more maintainable, understandable, and flexible software. Consequently, as our applications grow in size, we can reduce their complexity and save ourselves a lot of headaches further down the road.

## Single responsibility

Class should have only one responsibility,only one reason to change \(to be rewritten\), change only when specific part of specification changes. Responsibility should be encapsulated by class, module or function.

**WHY:**  
It makes class more robust \(krzepki\)

**HOW:**  
By encapsulation

**WHEN BREAKS:**  
When class, module or function has more than one responsibility or its name is not adequate to the behavior.  
When changing the code according changes from one specification/functionality breaks another specification/functionality

## Open / closed

Class should be open for extension, but closed for modification

You should be able to extend class's behavior without modifying it \(rewriting\)

**WHY:**  
Makes code maintainable and reusable

**HOW:**  
By abstraction. If system \(client\) will work with interface, it will work with any implementation of that interface

**WHEN BREAKS:**  
When adding new specification \(behavior\) there is a need to rewrite code base

## Liskov substitution

Assume that Q\(x\) means a property of instance **x**, and that **x** is of type T.  
Than we can say that Q\(y\) is the same property of instance **y** that is of type S,  
when S is subtype of T.

If it looks like a duck, quack like a duck but needs batteries - probably wrong abstraction

**WHY:**  
Any system should be working with any implementation of interface

**HOW:**   
By using pre-conditions of methods to be weaker and post-conditions to be stronger  
ex:   
pre-cond: base - work with int; sub - work with positive only int NOT WEAKER  
post-cond: base - work with positive int; sub - work with negative int NOT STRONGER

**WHEN BREAKS:**  
When add new subclass and not all properties or methods are applicable or methods should behave differently

## Interface segregation

It is better to have more smaller, client specific interfaces than fewer vast, more general ones

Big interface put al unnecessary properties on all lower hierarchy

Being small favoring Compose over Inheritance

It like with microservices: build lots of small responsibilities and compose them in large system

Too many is better than too few

**WHY:**  
Client should not be forced to use or implement functionalities that he doesn't need.

**HOW:**  
Split large interfaces into smaller and more specific ones \(role interfaces\)

**WHEN BREAKS:**  
When client needs to implement and stub unnecessary methods

## Dependency Inversion

High-level modules/classes should not depend on low-level modules/classes. Both should depend on abstraction \(interfaces/abstracts\)

Depend on abstraction, not on details \(implementation\)

**WHY:**  
Decouples modules/classes in system, increases reusability and flexibility of code.  
Increases testability because can inject mocks into another objects or methods

**HOW:**  
Extract behaviors, create abstraction of these behaviors and inject them as dependencies in "constructor injection" or "parameter injection"

**WHEN BREAKS:**  
"new" keyword is the signal for checking, instantiating low-level objects in methods or in another high-level objects

## SOURCES

{% embed url="https://hackernoon.com/solid-principles-made-easy-67b1246bcdf" %}

\(add linkedIn post to promote\)

