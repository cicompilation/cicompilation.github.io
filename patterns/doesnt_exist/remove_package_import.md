---
layout: page
---
## vavr-io/vavr 12.1

### Error Message

---------------------

```java
[ERROR] /home/travis/build/rocketscience-projects/rocket-java-extensions/src/main/java/io/rocketscience/java/lang/ObjectConverters.java:[6,28] package org.fest.util does not exist 
```

### Code Change

---------------------

***src/main/java/io/rocketscience/java/lang/ObjectConverters.java***

```diff
  import static java.util.stream.Collectors.toList;
- import static org.fest.util.Lists.newArrayList;
  import java.math.BigDecimal;
```