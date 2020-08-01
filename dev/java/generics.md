# Generics

Generics enable types to be parameters when defining classes, interfaces or methods  
Pros:

* stronger type checks
* no casts \(ArrayList&lt;Strong&gt;\)
* enable of implementing algorithms

### Generic type - Class&lt;T&gt;

* E - element used by collections
* K - key
* N - number
* T - type
* V - value

### Upper Bounded Wildcards

```text
public static void process(List<? extends Foo> list) { /* ... */ }
```

The upper bounded wildcard, &lt;? extends Foo&gt;, where Foo is any type, matches Foo and any **subtype** of Foo.

### Unbounded Wildcards

```text
public static void printList(List<Object> list) {
```

this only uses List of Objects, while 

```text
public static void printList(List<?> list) {
```

can use

```text
List<Integer> li = Arrays.asList(1, 2, 3);
List<String>  ls = Arrays.asList("one", "two", "three");
printList(li);
printList(ls);
```

### Lower Bounded Wildcards

```text
public static void addNumbers(List<? super Integer> list) {
```

method that works on lists of Integer and the **supertypes** of Integer, such as Integer, Number, and Object

