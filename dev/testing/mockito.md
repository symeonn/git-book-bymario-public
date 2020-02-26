# Mockito

given\(\) and then\(\) are BDD equivalents of when\(\) and verify\(\) respectively



* `when(...) thenReturn(...)` **makes a real method call** just before the specified value will be returned. So if the called method throws an Exception you have to deal with it / mock it etc. Of course you still get your result \(what you define in `thenReturn(...)`\) 
* `doReturn(...) when(...)` **does not call the method at all**. When spying real objects and calling real methods on a spy brings side effects, Overriding a previous exception-stubbing

