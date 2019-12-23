# unit-testing

Unit tests can be a code mass. It is not possible to make a 100% coverage. One cannot cover all possible loops, states wiet all possible input data.

Functional \(system\) tests should NOT be written by dev - code author.

In functional programming function was w code unit. It could be tested, it could be understood by reader, hence whole block of code or set of functions could be comprehended by reviewer.

In OO where responsibilities and data are encapsulated and moreover polymorphism occurs it is hard to reason about context in which the function is being computed. Those lines from context are not adjacent anymore like in procedural style.

Use UT for implementing, delete them later

UT only contract and integration tests

If UT fails what business requirement it affects?

