# unit testing

Unit tests can be a code mass. It is not possible to make a 100% coverage. One cannot cover all possible loops, states with all possible input data.

Functional (system) tests should NOT be written by dev - code author.

In functional programming function was w code unit. It could be tested, it could be understood by reader, hence whole block of code or set of functions could be comprehended by reviewer.

In OO where responsibilities and data are encapsulated and moreover polymorphism occurs it is hard to reason about context in which the function is being computed. Those lines from context are not adjacent anymore like in procedural style.

UT only contract and integration tests

If UT fails what business requirement it affects?

Write Unit test for implementation phase, later could be deleted, leave only those for main public methods.

UT is valuable when it fails - gives the information about system

Maybe instead of deleting UT tests after implementation, to keep them valuable, use PBT so UT every time will check something else, thus will be valuable

Tests to remove:

* Tests that never fails
* Tests that do not have to change when functionality change
* Tests always  true, valid
* Tests that when fails, we do not know what business requirement failed

more UT - more code to maintain

