# Collections



| Interfaces | Hash table Implementations | Resizable array Implementations | Tree Implementations | Linked list Implementations | Hash table + Linked list Implementations |
| ---------- | -------------------------- | ------------------------------- | -------------------- | --------------------------- | ---------------------------------------- |
| `Set`      | `HashSet`                  |                                 | `TreeSet`            |                             | `LinkedHashSet`                          |
| `List`     |                            | `ArrayList`                     |                      | `LinkedList`                |                                          |
| `Queue`    |                            |                                 |                      |                             |                                          |
| `Deque`    |                            | `ArrayDeque`                    |                      | `LinkedList`                |                                          |
| `Map`      | `HashMap`                  |                                 | `TreeMap`            |                             | `LinkedHashMap`                          |

## Implementations

### SET

#### HashSet

internal implementation is HashMap wit constant value="PRESENT"

#### TreeSet

internally uses TreeMap with constant value="PRESENT"

#### LinkedHashSet

### LIST

#### ArrayList

dynamical array stores value and index, internally it uses Object\[]

#### Linked list

each node has value and reference to the next node



### MAP

#### TreeMap

internally uses the implementation of red-black tree

## Big O notation (**Asymptotyczne tempo wzrostu)**

miara określająca zachowanie wartości funkcji wraz ze wzrostem ilości jej argumentów

![Big-O Complexity Chart](../../.gitbook/assets/image.png)

![Common Data Structure Operations](<../../.gitbook/assets/image (3) (2).png>)

![Array Sorting Algorithms](<../../.gitbook/assets/image (5).png>)

{% file src="../../.gitbook/assets/java-collections-cheat-sheet.pdf" %}

## equals() and hashMap()

\==  - operator for reference comparison, for primitives compares values\
equals() - method compares data/content od the object depending on implementation

### default implementation

equals() method is in Object class, compares if reference to the object is the same

hashCode() converts an internal object address into integer

### Contract

equals()

* REFLECTIVE - for any not-null a: a.equals(a) returns true
* SYMMETRIC - for any not-null a, b: a.equals(b) == b.equals(a)
* TRANSITIVE - for any not-null a, b, c: a.equals(b) and c.equals(c) => a.equals(c)
* CONSISTENT - for any not-null a, b: multiple calls a.equals(b) always return same boolean
* for any not-null a: a.equals(null) always return false

hashCode()

* IDEMPOTENCY - whencall hc() on the same object, it has to return same Integer every time if the object hasn't changed
* if two objects are equal (by equals() method) hc() has to return same HC
* it is **NOT** required that if two objects are **NOT **equal (by equals() method), hc() must produce distinct Integer, however it may improve performance (because different objects will be put into different buckets)&#x20;

### why override

equals()

* if not override, default implementation will be used that compared reference to objects
* when override hc() only, we may get same HC for different objects and and put into same bucket and it may decrease performance of search because objects are not equally distributed in the buckets

hashCode()

* if override only equals() we may get different HC for objects considered equal (by equals() method) hence comparison may return false for these objects
* not override hc() will break the contract
