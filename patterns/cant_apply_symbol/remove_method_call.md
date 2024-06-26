---
layout: page
---
## salesforce/storm-dynamic-spout 297.1

### Error Message

---------------------

```java
[ERROR] /home/travis/build/salesforce/storm-dynamic-spout/src/main/java/com/salesforce/storm/spout/sideline/handler/SidelineSpoutHandler.java:[75,9] constructor CustomMetric in class com.salesforce.storm.spout.dynamic.metrics.CustomMetric cannot be applied to given types; 
required: java.lang.String 
found: java.lang.String,java.lang.String 
reason: actual and formal argument lists differ in length 
```

### Code Change

---------------------

***src/main/java/com/salesforce/storm/spout/sideline/handler/SidelineSpoutHandler.java***

```diff
-    private static final CustomMetric startMetric =
-        new CustomMetric("SidelineSpoutHandler", "start-sideline");
```