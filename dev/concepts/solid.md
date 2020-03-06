# SOLID

## Single responsibility

class should have only one responsibility  
class should change only when specific part of specification change

## Open / close

Class should be open for extension but closed for modification  
polymorphism ?

## Liskov substitution

if it looks like a duck, quack like a duck but needs batteries - probably wrong abstraction

## Interface segregation

It is better to have more smaller, client specific interfaces than fewer vast, more general ones

Big interface put al unnecessary properties on all lower hierarchy

Being small favoring Compose over Inheritance

It like with microservices: build lots of small responsibilities and compose them in large system

Too many is better than too few

WHY:  
Client should not be forced to use functionalities that he doesn't need.

## Dependency Inversion

class should depend on adstraction not implementation

