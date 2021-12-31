# TDD

## Discipline for professionalism

### 3 laws

* NO production code before failing unit test
* write only ENOUGH test code to demonstrate the failure
* write only ENOUGH production code to make failing test to pass&#x20;

### 3 phases

* RED
* GREEN
* REFACTOR

TDD neglects the fear of change

TDD created low level documentation that is always up to date&#x20;

TDD creates testable and decoupled production code

When in GREEN phase, even though we could take shortcut and make the test pass right away, it is good to return failed value to make sure that the test will fail and then, right away, return the correct to make the test pass. In this way we know that this test can fail

Whenever you write code and need to add static variable or flag, something must be wrong with the design

it is common to delete tests when progressing with TDD - these are not valid anymore

if there is something wrong with the design or you cannot make the test pass easily, step back one, Ignore the test and refactor previous written code

