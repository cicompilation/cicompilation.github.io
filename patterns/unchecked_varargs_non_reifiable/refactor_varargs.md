---
layout: page
---
## OryxProject/oryx  297.2

### Warning Message

---------------------

```java
[WARNING] /home/travis/build/OryxProject/oryx/oryx-common/src/main/java/com/cloudera/oryx/common/collection/AndPredicate.java:[25,45] Possible heap pollution from parameterized vararg type com.carrotsearch.hppc.predicates.ObjectPredicate<T>
```

### Code Change

---------------------

***.travis.yml***

```diff
-  public AndPredicate(ObjectPredicate<T>... clauses) {
-    Preconditions.checkNotNull(clauses);
-    Preconditions.checkArgument(clauses.length > 0);
-    this.clauses = clauses;
+  public AndPredicate(ObjectPredicate<T> a, ObjectPredicate<T> b) {
+    this.a = a;
+    this.b = b;
  }
```