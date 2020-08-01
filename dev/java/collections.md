# Collections



| Interfaces | Hash table Implementations | Resizable array Implementations | Tree Implementations | Linked list Implementations | Hash table + Linked list Implementations |
| :--- | :--- | :--- | :--- | :--- | :--- |
| `Set` | `HashSet` |   | `TreeSet` |   | `LinkedHashSet` |
| `List` |   | `ArrayList` |   | `LinkedList` |   |
| `Queue` |   |   |   |   |   |
| `Deque` |   | `ArrayDeque` |   | `LinkedList` |   |
| `Map` | `HashMap` |   | `TreeMap` |   | `LinkedHashMap` |

## Implementations

### SET

#### HashSet

internal implementation is HashMap wit constant value="PRESENT"

#### TreeSet

internally uses TreeMap with constant value="PRESENT"

#### LinkedHashSet

### LIST

#### ArrayList

dynamical array stores value and index, internally it uses Object\[\]

#### Linked list

each node has value and reference to the next node



### MAP

#### TreeMap

internally uses the implementation of red-black tree

## Big O notation \(**Asymptotyczne tempo wzrostu\)**

miara określająca zachowanie wartości funkcji wraz ze wzrostem ilości jej argumentów

![Big-O Complexity Chart](../../.gitbook/assets/image.png)

![Common Data Structure Operations](../../.gitbook/assets/image%20%283%29%20%282%29.png)

![Array Sorting Algorithms](../../.gitbook/assets/image%20%285%29.png)

{% file src="../../.gitbook/assets/java-collections-cheat-sheet.pdf" %}

