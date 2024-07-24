---
layout: page
---
## chrisvest/stormpot 56.2

### Warning Message

---------------------

```java
[WARNING] /home/travis/build/chrisvest/stormpot/src/test/java/stormpot/adaptors/SelfCleaningPoolTest.java:[60,24] unchecked generic array creation for varargs parameter of type java.lang.Class<? extends java.lang.Throwable>[]


```

### Code Change

---------------------

***src/test/java/stormpot/adaptors/SelfCleaningPoolTest.java***

```diff
-       // a self-cleaning pool, configured to work faster than normal
-       cleaningPool = new SelfCleaningPool<Poolable>(mockPool,threadPool,1,RuntimeException.class);
```