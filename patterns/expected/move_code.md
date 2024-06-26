---
layout: page
---
## caskdata/coopr 220.1

### Error Message

---------------------

```java
[ERROR] /home/travis/build/continuuity/loom/server/src/main/java/com/continuuity/loom/http/handler/LoomPluginHandler.java:[668,23] ';' expected
```

### Code Change

---------------------

***server/src/main/java/com/continuuity/loom/http/handler/LoomPluginHandler.java***

```diff
- <<<<<<< HEAD
-        responder.sendError(HttpResponseStatus.INTERNAL_SERVER_ERROR, "Error activating module version.");
-      } catch (MissingEntityException e) {
-        responder.sendError(HttpResponseStatus.NOT_FOUND, e.getMessage());
-  =======
       LOG.error("Exception deleting all versions of resource.", e);
       responder.sendError(HttpResponseStatus.INTERNAL_SERVER_ERROR, "Error deleting all versions of resource.");
-  >>>>>>> origin/develop
+     } catch (MissingEntityException e) {
+       responder.sendError(HttpResponseStatus.NOT_FOUND, e.getMessage());
```