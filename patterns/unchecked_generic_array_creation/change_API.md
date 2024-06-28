---
layout: page
---
## apache/bookkeeper 1235.4

### Warning Message

---------------------

```java
[WARNING] /home/travis/build/apache/bookkeeper/bookkeeper-server/src/test/java/org/apache/bookkeeper/client/api/BookKeeperApiTest.java:[251,43] unchecked generic array creation for varargs parameter of type org.hamcrest.Matcher<? super org.apache.log4j.spi.LoggingEvent>[]

```

### Code Change

---------------------

***.travis.yml***

```diff
-            assertThat(logEvents, hasItems(hasProperty("renderedMessage",
+            assertThat(logEvents, hasItem(hasProperty("renderedMessage",
```