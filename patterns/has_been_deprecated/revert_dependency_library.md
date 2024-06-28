---
layout: page
---
## uber/tchannel-java 874.1

### Warning Message

---------------------

```java
[WARNING]/home/travis/build/ubeer/tchannel-java/tchannel-core/src/main/java/com/uber/tchannel/tracing/Tracing.java:[81,34] startManual() in io.opentracing.Tracer.SpanBuer has been deorecated
```

### Code Change

---------------------

***pom.xml***

```diff
                 <groupId>io.opentracing</groupId>
                 <artifactId>opentracing-api</artifactId>
-                <version>0.31.0</version>
+                <version>0.30.0</version>
```