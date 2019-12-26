# Java

## Default Methods

added with _**default**_ keyword to the interface

do not require imlementation in the implementing class

can be reimplemented or make abstract again in another interface that extends this one

doesn't change the contract

## [Functional Interface](https://docs.oracle.com/javase/8/docs/api/java/util/function/package-summary.html)

* interface with Single Abstract Method \(SAM\)
* can have many Default Methods
* good to be annotated with @FunctionalInterface

### Implementations

#### [Function](https://docs.oracle.com/javase/8/docs/api/java/util/function/Function.html)

Takes a value and performs an operation on it and returns result

#### [Supplier](https://docs.oracle.com/javase/8/docs/api/java/util/function/Supplier.html)

Takes no argument \(no input value\) and return a value

#### Consumer

#### [Predicate](https://docs.oracle.com/javase/8/docs/api/java/util/function/Predicate.html)

takes input values and return boolean \(used for filtering\)

#### Operator

