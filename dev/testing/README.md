# Testing

## Think TEST-FIRST

### Division of tests

Tests by level:

* Unit tests - developer perspective tests, helps build the product right (verification)
* Integration tests - test communication between modules or systems
* System tests

Tests by testing methods:

* Black-box testing - behavioral testing, INPUT and OUTPUT matters
* White-box testing - choose INPUT that goes through the code (Unit testing)

Tests by type:

* Regression testing - ensures that changes to the software does not brake any part of it
* Performance testing
* Functional testing - testing requirements/specifications (functions) of the application, UI testing, user perspective tests, helps build the right product (validation)
* Smoke testing - Build Verification Testing, light part of test just to confirm that app is bootable and most important functions work, build is stable enough for further testing

### TDD

test is written to check the implementation of functionality

We don’t care much about the output. The only thing needed is to carry out the test in a particular way.

Internal application tests

#### Testy inkrementacyjne

* first simple naive test
* then more complex tests
* finally whole component tests

### BDD

testing the actual behavior of the system from the end users perspective

We don’t mind how you come up with the output, only that the output has to be correct under the GIVEN condition.

External application tests

business people do not want to do the BDD

business rules are tested

### SOURCES

[https://softwaretestingfundamentals.com/](https://softwaretestingfundamentals.com)
