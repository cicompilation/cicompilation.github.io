---
layout: page
---
## maxcom/lorsource 2456.1

### Warning Message

---------------------

```java
/home/travis/.m2/repository/con/gogle/guava/guava/21.0/guava-21.0.iar(con/gogle/comon/colect/Mutimap.class):warning:Cannot find anotation method'value()'in type 'Compatiblewith':class file for com.google.errorprone.annotations.CompatibleWith not found

```

### Code Change

---------------------

***pom.xml***

```diff
      <groupId>com.google.guava</groupId>
      <artifactId>guava</artifactId>
-     <version>21.0</version>
+     <version>20.0</version>
```