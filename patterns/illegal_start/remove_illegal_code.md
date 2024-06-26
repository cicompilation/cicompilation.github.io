---
layout: page
---
## naver/pinpoint 309.1

### Error Message

---------------------

```java
[ERROR] /home/travis/build/naver/pinpoint/web/src/main/java/com/navercorp/pinpoint/web/controller/MapController.java:[199] illegal start of expression
```

### Code Change

---------------------

***web/src/main/java/com/navercorp/pinpoint/web/controller/MapController.java***

```diff
- <<<<<<< HEAD
-    final Application sourceApplication = new Application(sourceApplicationName, sourceServiceType);
-    final Application destinationApplication = new Application(targetApplicationName, targetServiceType);
- =======
    final Application sourceApplication = new Application(sourceApplicationName, registry.findServiceTypeByName(sourceServiceTypeName));
    final Application destinationApplication = new Application(targetApplicationName, registry.findServiceTypeByName(targetServiceTypeName));
- >>>>>>> 18c9bcf... added request mappings to support serviceTypeName parameters
    final Range range = new Range(from, to);
```