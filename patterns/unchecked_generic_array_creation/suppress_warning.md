---
layout: page
---
## jOOQ/jOOL 222.1

### Warning Message

---------------------

```java
[WARNING] /home/travis/build/jOOQ/jOOL/src/test/java/org/jooq/lambda/SeqTest.java:[1396,39] [unchecked] unchecked generic array creation for varargs parameter of type Optional<? extends Integer>[]

```

### Code Change

---------------------

***src/main/java/org/jooq/lambda/Seq.java***

```diff
+   @SafeVarargs
    static <T> Seq<T> seq(Optional<? extends T>... optionals) {
```