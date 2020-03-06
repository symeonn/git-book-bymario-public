---
description: >-
  design principles encourage us to create more maintainable, understandable,
  and flexible software. Consequently, as our applications grow in size, we can
  reduce their co
---

# SOLID

## Single responsibility

class should have only one responsibility  
class should change only when specific part of specification change

WHY:

HOW:

WHEN breaks:

## Open / close

Class should be open for extension but closed for modification

You should be able to extend class's behavior without modifying it \(rewriting\)

WHY:  
makes code maintainable and reusable

HOW:  
By abstraction. If system \(client\) will work with interface, it will work with any implementation of that interface

WHEN breaks:  
When adding new specification \(behavior\) there is a need to rewrite code base

## Liskov substitution

Assume that Q\(x\) means a property of instance **x**, and that **x** is of type T.  
Than we can say that Q\(y\) is the same property of instance **y** that is of type S,  
when S is subtype of T.

If it looks like a duck, quack like a duck but needs batteries - probably wrong abstraction

WHY:

HOW:

WHEN breaks:  
when add new subclass and it comes that not all properties or methods are applicable or methods should behave differently

## Interface segregation

It is better to have more smaller, client specific interfaces than fewer vast, more general ones

Big interface put al unnecessary properties on all lower hierarchy

Being small favoring Compose over Inheritance

It like with microservices: build lots of small responsibilities and compose them in large system

Too many is better than too few

WHY:  
Client should not be forced to use functionalities that he doesn't need.

HOW:

WHEN breaks:

## Dependency Inversion

class should depend on adstraction not implementation

WHY:

HOW:

WHEN breaks:

#### SOURCE:

{% embed url="https://hackernoon.com/solid-principles-made-easy-67b1246bcdf" %}

\(add linkedIn post to promote\)

