---
layout: page
---
## benas/random-beans  69.1

### Warning Message

---------------------

```java
[WARNING] /home/travis/build/benas/random-beans/random-beans/src/main/java/io/github/benas/randombeans/ExclusionDefinitionBuilder.java:[51,16] unchecked call to ExclusionDefinition(java.lang.String,java.lang.Class<F>,java.lang.Class<T>) as a member of the raw type io.github.benas.randombeans.ExclusionDefinition

```

### Code Change

---------------------

***random-beans/src/main/java/io/github/benas/randombeans/ExclusionDefinitionBuilder.java***

```diff
-  public ExclusionDefinition get() {
-        return new ExclusionDefinition(name, type, clazz);
-    }
```