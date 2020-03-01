# Testing

### Division of tests

Tests by level:

* Unit tests
* Integration tests
* System tests

Tests by testing metchods:

* Black-box testing - behavioral testing, INPUT and OUTPUT matters
* White-box testing - choose INPUT that goes through the code \(Unit testing\)

Tests by type:

* Regression testing - ensures that changes to the software does not brake any part of it
* Performance testing
* Functional testing - testing requirements/specifications \(functions\) of the application
* Smoke testing - Build Verification Testing, light part of test just to confirm that app is bootable and most important functions work, build is stable enough for further testing

in new \(which?\) version of Mockito when use anyString\(\) or any\(String.class\) etc. it will not mock the method if there will be null send as parameter. For that any\(\) have to be used.

### TDD

test is written to check the implementation of functionality

 We don’t care much about the output. The only thing needed is to carry out the test in a particular way.

### BDD

testing the actual behavior of the system from the end users perspective

We don’t mind how you come up with the output, only that the output has to be correct under the GIVEN condition.

