---
layout: page
---
## thinkaurelius/titan 14.1


### Error Message

---------------------

```java
[ERROR] TitanBlueprintsTransaction.java:[22,4] method does not override or implement a method from a supertype 
```

### Code Change

---------------------

***src/main/java/com/thinkaurelius/titan/graphdb/blueprints/TitanBlueprintsTransaction.java***

```diff
-  @Override
-   public void startTransaction() throws IllegalStateException {
-       //Do nothing, transaction already started
-   }
```