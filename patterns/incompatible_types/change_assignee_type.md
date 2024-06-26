---
layout: page
---
## rockscript/rockscript 4.1

### Error Message

---------------------

```java
[ERROR] /home/travis/build/RockScript/server/engine/src/test/java/io/rockscript/action/http/HttpActionTest.java:[46,70] incompatible types: java.util.List<io.rockscript.engine.ExecutionEventJson> cannot be converted to java.util.List<io.rockscript.engine.EventJson>
```

### Code Change

---------------------

***engine/src/test/java/io/rockscript/action/http/HttpActionTest.java***

```diff
    // Then the action execution created an action ended event with the result
-   List<EventJson> events = eventStore.findEventsByScriptExecutionId(scriptExecutionId);
+   List<ExecutionEventJson> events = eventStore.findEventsByScriptExecutionId(scriptExecutionId);
    assertNotNull(events);
    assertFalse(events.isEmpty());
    Response httpResponse = events.stream()
```