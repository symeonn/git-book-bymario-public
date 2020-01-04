# Contract testing

### Publisher

* regular UT
* sends the message to the queue and tests message with mocked template \(in groovy file\)

### Consumer

* generated UT \(by framework\)
* mocks incoming message to listener and compare a mocked message fields
* uses generated stub.jar

