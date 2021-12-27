# TDD

### 3 laws

* NO production code before test code
*

### 3 phases

* RED
* GREEN
* REFACTOR

When in GREEN phase, even though we could take shortcut and make the test pass right away, it is good to return failed value to make sure that the test will fail and then, right away, return the correct to make the test pass. In this way we know that this test can fail

Whenever you write code and need to add static variable or flag, something must be wrong with the design

it is common to delete tests when progressing with TDD - these are not valid anymore

if there is something wrong with the design or you cannot make the test pass easily, step back one, Ignore the test and refactor previous written code
