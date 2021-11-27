# Clean Code

## Take from NOTION



## Function Structure

continuing...

### side effects

if global variables or overall state is influencing lots on places it causes the method to be called in certain order (is this a part of [#procedural-programming](../dev/concepts/paradigms.md#procedural-programming "mention") ?) - this is temporary coupling to the application state

Solution: **passing the block**. Passing as a method argument the block of commands, ie. hiding dependent method in another method

Another solution: **separate commands and queries **(example: setters and getters)** **

* commands: changes the state of the system, it has a side effect
* queries: returns the value of the computation or state of the system

### do not return NULL - throw exceptions instead

### Tell, Don't Ask

tell objects what to do, but do not ask them what is their state
