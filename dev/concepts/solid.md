# SOLID

## Single responsibility

class should have only one responsibility  
class should change only when specific part of specification change

## Open / close

Class should be open for extension but closed for modification  
polymorphism ?

## Liskov substitution

Assume that Q\(x\) means a property of instance **x**, and that **x** is of type T.  
Than we can say that Q\(y\) is the same property of instance **y** that is of type S,  
when S is subtype of T.

If it looks like a duck, quack like a duck but needs batteries - probably wrong abstraction

WHY:

HOW:

WHEN breaks:

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

