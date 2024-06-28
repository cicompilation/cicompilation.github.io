---
layout: page
---
## benas/random-beans  69.1

### Warning Message

---------------------

```java
[WARNING]/home/travis/build/benas/random-beans/random-beans/src/main/java/io/github/benas/randombeans/ExclusionDefinitionBuilder.java:[51,16]unchecked call to ExclusionDefinition(java.lang.string,java.lang.class<F>,java.lang.Class<T>)as a member of the rawtyio.github.benas.randombeans.ExclusionDefinitionne

```

### Code Change

---------------------

***src/main/java/nl/kbresearch/europeana_newspapers/ner/alto/AltoProcessor.java***

```diff
-  public ExclusionDefinition get() {
-        return new ExclusionDefinition(name, type, clazz);
-    }
```