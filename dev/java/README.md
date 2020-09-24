# Java

## Default Methods

added with _**default**_ keyword to the interface

do not require imlementation in the implementing class

can be reimplemented or make abstract again in another interface that extends this one

doesn't change the contract

## [Functional Interface](https://docs.oracle.com/javase/8/docs/api/java/util/function/package-summary.html)

[@FunctionalInterface](https://docs.oracle.com/javase/8/docs/api/java/lang/FunctionalInterface.html) is example of utilizing functional programming paradigm in Java.  
It is used by lambda expressions.

Conceptually, a functional interface has exactly one abstract method.

* interface with Single Abstract Method \(SAM\)
* can have many Default Methods
* all have one or two input operators variants
* all have versions for primitive types

### Implementations

#### [Function](https://docs.oracle.com/javase/8/docs/api/java/util/function/Function.html)

Takes a value and performs an operation on it and returns result

#### [Supplier](https://docs.oracle.com/javase/8/docs/api/java/util/function/Supplier.html)

Takes no argument \(no input value\) and return a value

#### [Consumer](https://docs.oracle.com/javase/8/docs/api/java/util/function/Consumer.html)

takes input values but do not return any \(used for side effects\)

#### [Predicate](https://docs.oracle.com/javase/8/docs/api/java/util/function/Predicate.html)

takes input values and return boolean \(used for filtering\)

#### [Operator](https://docs.oracle.com/javase/8/docs/api/java/util/function/BinaryOperator.html)

Take input values and return value of the same type \(reduce\)

### Best practices

* always annotate with @FunctionalInterface
* do not overuse Default Methods \(?\)
* lambdas are not Inner Classes
* use built-in interfaces from java.util.function
* do not overload methods with FI as more params
* Instantiate FI with lambdas \(not classes\)
* keep lambda short:
  * do not use \(\) for one argument functions
  * do not use multiline functions in lambda
  * do not use _**return**_ and {} in one line functions
  * do not state parameter type \(?\)
  * use method reference \(ex: String::toLowerCase\)
* use _**effective final**_ in lambdas - it is variable that is assigned once so it is implied "final"

