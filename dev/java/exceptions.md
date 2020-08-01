# Exceptions

![](../../.gitbook/assets/image%20%287%29.png)

### Error

exceptions from JVM or caused by system \(infrastructure error\), should not recover the system

ex: OutOfMemoryError

### RuntimeExceptions

exceptions happen in the runtime, usually means the bug in the system or logic error

ex: NullPointerException, IndexOutOfBountException

### Checked exceptions

all exceptions from class Exception, except those RuntimeExceptions \(so Errors are also not a checked\), should be caught and anticipated, mandatory to be thrown by methods

FileNotFountException, IOException

### Unchecked exceptions

Error and RuntimeExceptions, not mandatory to be thrown by methods



