---
layout: page
---
## zalando/riptide  10.1

### Warning Message

---------------------

```java
[WARNING] /home/travis/build/zalando/riptide/src/main/java/org/zalando/riptide/RestDispatcher.java:[97,83] Possible heap pollution from parameterized vararg type org.zalando.riptide.Binding<A,?,O>

```

### Code Change

---------------------

***src/main/java/org/zalando/riptide/RestDispatcher.java***

```diff
- public final <A, O> ResponseExtractor<ResponseEntity<O>> dispatch(Selector<A> selector,
-                                                                      Binding<A, ?, O> first,
-                                                                      Binding<A, ?, O> second,
-                                                                      Binding<A, ?, O>... rest) {
```