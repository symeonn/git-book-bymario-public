# Generics

Generics enable types to be parameters when defining classes, interfaces or methods\
Pros:

* stronger type checks
* no casts (ArrayList\<Strong>)
* enable of implementing algorithms

### Generic type - Class\<T>

* E - element used by collections
* K - key
* N - number
* T - type
* V - value

### Upper Bounded Wildcards

```
public static void process(List<? extends Foo> list) { /* ... */ }
```

The upper bounded wildcard, \<? extends Foo>, where Foo is any type, matches Foo and any **subtype **of Foo.

### Unbounded Wildcards

```
public static void printList(List<Object> list) {
```

this only uses List of Objects, while&#x20;

```
public static void printList(List<?> list) {
```

can use

```
List<Integer> li = Arrays.asList(1, 2, 3);
List<String>  ls = Arrays.asList("one", "two", "three");
printList(li);
printList(ls);
```

### Lower Bounded Wildcards

```
public static void addNumbers(List<? super Integer> list) {
```

method that works on lists of Integer and the **supertypes **of Integer, such as Integer, Number, and Object
