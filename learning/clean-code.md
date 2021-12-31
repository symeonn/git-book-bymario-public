# Clean Code

{% embed url="https://learning.oreilly.com/videos/clean-code-fundamentals/9780134661742" %}

## Names

* do not disinform
* if comment is needed - name is bad
* make lines to be read like a sentences
* whenever you need to go to the code to look the implementation, the name is bad
* scope length = name length (for variables) - broader scope ⇒ longer name, smaller scope ⇒ shorter name
* scope length ≠ name length (for functions - public functions will be used in lot of places) - broader scope ⇒ shorter name, smaller scope ⇒ longer, self explanatory name

## Functions

* they are small
* classes hide in long functions (use '**Extract to Method Object**' refactor option)
* line intends signals refactor need
* do not mix technical implementation concerns with business concerns - separate low level implementation details (programing stuff) and high level of business concepts, do not let one function manipulate both concepts
* if function manipulate its parameter it should be moved to that class (Feature Envy smell)
* Code coverage to see what code is user and what is not (**CHECK**)

## Function Structure

* the less arguments the better (max 3)
* no Boolean arguments - it means function does two things, write 2 functions instead, one for TRUE and one of FALSE
* do not use output arguments (argument that will be changed in function), it causes confusions - use return
* do not pass NULL or do not write functions that expect NULL (two states as boolean - for NULL and non-NULL) - write two functions instead, for each case
* above is **Defencing Programming, a code smell** (not applying to public API where you need to validate)
* **Stepdown Rule** - public methods goes at the top and preferably call hierarchy is reflected in methods order (in code: up - more abstract; down more detailed)
* SWITCH statement are no OOP and it is missed opportunity to use polymorphism
  * A: Dependency between objects (cannot be deployed separately):![](<../.gitbook/assets/image (13).png>)
  * B: using OO we can change source code dependency (can be deployed separately):![](<../.gitbook/assets/image (12).png>)
  * SWITCH is considered to be a A solution (a fan-out problem) - each CASE is like separate module so SWITCH creates dependencies to these modules
  * solutions:
    * change to polimorphism:
      * take argument of the SWITCH and refactor it to abstract base class with method that correspond to the operation of the SWITCH
      * each CASE statements will be derivative of this abstract base class
    * move them where they cannot do any harm, do not create dependencies so cannot be deploy separately) - rather im MAIN part on below image (the APP is a core and the MAIN is plugin, APP should not know anything about main)![](<../.gitbook/assets/image (16).png>)
* the same goes for IF statements
* Paradigms [paradigms.md](../dev/concepts/paradigms.md "mention")
  * [#functional-programming](../dev/concepts/paradigms.md#functional-programming "mention")
  * [#structured-programming](../dev/concepts/paradigms.md#structured-programming "mention")
  * [#object-oriented-programming](../dev/concepts/paradigms.md#object-oriented-programming "mention")
* side effects
  * if global variables or overall state is influencing lots on places it causes the method to be called in certain order (is this a part of [#procedural-programming](../dev/concepts/paradigms.md#procedural-programming "mention") ?) - this is temporary coupling to the application state
  * Solution: **passing the block**. Passing as a method argument the block of commands, ie. hiding dependent method in another method
  * Another solution: **separate commands and queries** (example: setters and getters) ****&#x20;
    * commands: changes the state of the system, it has a side effect
    * queries: returns the value of the computation or state of the system
* do not return NULL to indicate error, throw exceptions instead - when method needs to return NULL (ex. find - nothing has been found) but not to indicate the error, caller can/should expect NULL from that function **NULL MEANS NOTHING**
* Tell, Don't Ask
  * tell objects what to do, but do not ask them what is their state
  * we ask also about objects in objects and this leads to **Train Wrecks** (o.getX().getZ().getY().doSomething())  it valioates **Law of Demeter** (too much knowledge in single line)
*   Error Handling

    * write EH first before rest of the code
    * prefer throwing exception instead return null or false&#x20;
    * exception should be scoped to the context of the caller and named with specific information possible
    * use unchecked exception, extend RuntimeException - it creates dependencies (ex. method that throws exception is changed)
    * try block rules:
      * try should be the first word in the function after variable declaration
      * there should be single line in body of the try block
      * catch and finally should be last statements in the method
    * error handling is one thing so method should do some computation or handle errors, never both (??)



## Form

#### Comments

* do not use comments
* if you find the comment - remove it
* if you must comment - do it locally
* commented out code? REMOVE

#### Classes

from the outside perspective classes are a set of methods

Cohesive class - the class that has methods that operate on as much as possible (private) class variables&#x20;

getters and setters do not produce cohesive classes because they operate only on one variable each

instead getters or setters - abstract the access to internal variables, this will increase polymorphism and independent deploybility&#x20;

Object protects client from new types - derivative object can be still used in place of parent object\
add new type all SWITCH needs to be modified - do not use SWITCH on objects

but do not protect from new method (behavior) - add new methods all child classes needs to be compiled

user classes with behaviors when more types to be added later

#### Data structure

opposite to the class has public variables (via getters and setters) and has no methods (no behavior), do not put business rules in them

Data structure protects from new methods - when adding new one, just add new method with new SWITCH (added not on data structure but somewhere else)

But when adding new data structure type - need to change all SWITCH that are depend on them

user Data structures and switch statements when new methods to be added later on

#### Boundaries

they separate abstract and concrete parts of code, in a way that abstract should not depend on concrete but **concrete should depend on abstract** (code dependency)

Examples:

* main (concrete) separate from app (abstract)
* view (concrete) separates from models (abstract)
* BD (concrete) from domain objects (abstract)

Can use intermidiate layer to separate layers (create boundaries)

## TDD

see [tdd.md](../dev/testing/tdd.md "mention")

## Architecture

see [architecture.md](../dev/design/architecture.md "mention")

## &#x20;
