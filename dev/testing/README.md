# Testing

## Think TEST-FIRST

### Division of tests

Tests by level:

* Unit tests
* Integration tests
* System tests

Tests by testing methods:

* Black-box testing - behavioral testing, INPUT and OUTPUT matters
* White-box testing - choose INPUT that goes through the code (Unit testing)

Tests by type:

* Regression testing - ensures that changes to the software does not brake any part of it
* Performance testing
* Functional testing - testing requirements/specifications (functions) of the application
* Smoke testing - Build Verification Testing, light part of test just to confirm that app is bootable and most important functions work, build is stable enough for further testing

### TDD

test is written to check the implementation of functionality

&#x20;We don’t care much about the output. The only thing needed is to carry out the test in a particular way.

#### Testy inkrementacyjne

* first simple naive test
* then more complex tests
* finally whole component tests

### BDD

testing the actual behavior of the system from the end users perspective

We don’t mind how you come up with the output, only that the output has to be correct under the GIVEN condition.

*

### SOURCES

[https://softwaretestingfundamentals.com/](https://softwaretestingfundamentals.com)
