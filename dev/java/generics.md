# Generics

## Upper Bounded Wildcards



```text
public static void process(List<? extends Foo> list) { /* ... */ }
```

The upper bounded wildcard, &lt;? extends Foo&gt;, where Foo is any type, matches Foo and any subtype of Foo.



