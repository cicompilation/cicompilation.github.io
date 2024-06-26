---
layout: page
---
## xetorthio/jedis 600.1

### Error Message

---------------------

```java
[ERROR] /home/travis/build/xetorthio/jedis/src/main/java/redis/clients/jedis/params/Params.java:[25,28] illegal start of type 
```

### Code Change

---------------------

***src/main/java/redis/clients/jedis/params/Params.java***

```diff
    if(params == null) {
-      params = new HashMap<>();
+      params = new HashMap<String, Object>();
     }
```