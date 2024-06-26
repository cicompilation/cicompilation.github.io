---
layout: page
---
## orbit/orbit  28.1

### Error Message

---------------------

```java
[ERROR]  /home/travis/build/electronicarts/orbit/actors/core/src/main/java/com/ea/orbit/actors/ObserverManager.java:[93,37] cannot find symbol 
symbol: method ping() 
location: variable o of type T 
```

### Code Change

---------------------

***actors/core/src/main/java/com/ea/orbit/actors/ObserverManager.java***

```diff
  final Stream<Task<?>> stream = observers.stream()
                .map(o ->
-                       ((Task<?>) o.ping()).whenComplete((final Object pr, final Throwable pe) ->
+                       ((Task<?>) ((IAddressable)o).ping()).whenComplete((final Object pr, final Throwable pe) ->

```