# Paradigms

## Functional Programming

* use function without side-effects
* only return the result and combine with another and set as parameter of another function
* Avoid changing state or mutation.
* do not use assignment statements
* functions are true mathematical function - always return the same value for the same input (no global or side state is taken into consideration)
*

[Functional programming in java.](../java/#functional-interface)

## Procedural Programming

use functions or blocks of code in desired order to build functionality, eg:

```
void getEntity() {
    verifyUser();
    validateAccess();
    accuireEntities();
    processEntity();
    notifyUser();
}
```

(is above an antipattern??)

## Structured Programming

All algorithms should be composed of 3 elements, having single entrance on the top and single exit at the bottom (one return statement, at best):

* sequence - arrangement of two blocks, exit of the first one feeds entry of the second
* selection - boolean that breaks the flow to different blocks
* iteration - repeated execution of the block, until exit statement is satisfied

If you compose the algorithm of these 3 blocks, they may be sequential because they do not depend on each other

## Object-Oriented Programming

functionalities and data are encapsulated into objects. Selection of objects happens in the runtime



## Declarative Programming

