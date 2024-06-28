---
layout: page
---
## Netflix/servo 119.1

### Warning Message

---------------------

```java
:servo-core:compilerestJava/home/travis/ouild/Netflix/sero/servo-core/src/test/java/con/netflix/sero/mnitor/MonitorsTest.java:126:warning:[unchecked] uncheck conversion
List<Monitor>monitors =compositeMonitor.getMonitors();
required:List<Monitor>
found:List

```

### Code Change

---------------------

***servo-core/src/test/java/com/netflix/servo/monitor/MonitorsTest.java***

```diff
+    @SuppressWarnings("unchecked")
     List<Monitor> monitors = compositeMonitor.getMonitors();
```