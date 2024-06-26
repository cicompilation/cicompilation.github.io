---
layout: page
---
## salesforce/storm-dynamic-spout 188.1

### Error Message

---------------------

```java
[ERROR] /home/travis/build/salesforce/storm-dynamic-spout/src/test/java/com/salesforce/storm/spout/dynamic/coordinator/SpoutMonitorTest.java:[145,43] constructor SpoutMonitor in class com.salesforce.storm.spout.dynamic.coordinator.SpoutMonitor cannot be applied to given types; 
required: java.util.Map<java.lang.String,java.lang.Object>,com.salesforce.storm.spout.dynamic.VirtualSpoutMessageBus,com.salesforce.storm.spout.dynamic.metrics.MetricsRecorder
found: com.salesforce.storm.spout.dynamic.MessageBus,java.time.Clock,java.util.Map<java.lang.String,java.lang.Object>,com.salesforce.storm.spout.dynamic.metrics.MetricsRecorder 
reason: actual and formal argument lists differ in length 
```

### Code Change

---------------------

***src/test/java/com/salesforce/storm/spout/dynamic/coordinator/SpoutMonitorTest.java***

```diff
        final SpoutMonitor spoutMonitor = new SpoutMonitor(
-            messageBus,
-            clock,
             topologyConfig,
+            messageBus,
             metricsRecorder
         );
```