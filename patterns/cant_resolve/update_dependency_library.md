---
layout: page
---
## google/guava 1302.1

### Error Message

---------------------

```java
[ERROR] [ERROR] [ERROR] /home/travis/build/google/guava/guava-gwt/test/com/google/common/collect/IteratorsTest_gwt.java:[93,10] error: cannot find symbol 

[ERROR] variable testCase of type IteratorsTest 
```

### Code Change

---------------------

***guava-gwt/pom.xml***

```diff
  <parent>
    <groupId>com.google.guava</groupId>
    <artifactId>guava-parent</artifactId>
-   <version>22.0-SNAPSHOT</version>
+   <version>23.0-SNAPSHOT</version>
  </parent>

```