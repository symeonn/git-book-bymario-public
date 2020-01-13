# JUnit 5

## Main parts

* Jupiter \(JUnit 5\)
* Vintage \(compability with JUnit4\)
* platform \(for plugins\)

## Thoughts

no _public_ methods - less to write  
meta-adnotations  
Test Info \(additional info about test\)  
assume \(?\)

## PowerMock and Mockito supported versions

PowerMock version 2.0.0 and upper has support of Mockito 2. PowerMock version 1.7.0 and upper has experimental support of Mockito 2.

A lot of issues are not resolved still. PowerMock uses internal Mockito API, but at least it possible to use both mocking framework together.

| **Mockito** | **PowerMock** |
| :--- | :--- |
| 2.8.9+ | 2.x |
| 2.8.0-2.8.9 | 1.7.x |
| 2.7.5 | 1.7.0RC4 |
| 2.4.0 | 1.7.0RC2 |
| 2.0.0-beta - 2.0.42-beta | 1.6.5-1.7.0RC |
| 1.10.8 - 1.10.x | 1.6.2 - 2.0 |
| 1.9.5-rc1 - 1.9.5 | 1.5.0 - 1.5.6 |
| 1.9.0-rc1 & 1.9.0 | 1.4.10 - 1.4.12 |
| 1.8.5 | 1.3.9 - 1.4.9 |
| 1.8.4 | 1.3.7 & 1.3.8 |
| 1.8.3 | 1.3.6 |
| 1.8.1 & 1.8.2 | 1.3.5 |
| 1.8 | 1.3 |
| 1.7 | 1.2.5 |

