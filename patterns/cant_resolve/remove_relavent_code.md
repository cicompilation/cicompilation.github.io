---
layout: page
---
## xetorthio/jedis 700.1

### Error Message

---------------------

```java
[ERROR] /home/travis/build/xetorthio/jedis/src/main/java/redis/clients/jedis/JedisCluster.java:[591,68] cannot find symbol 
symbol : variable timeout 
location: class redis.clients.jedis.JedisCluster 
```

### Code Change

---------------------

***src/org/nutz/rpc/json/JsonRpcException.java***

```diff
  public Set<String> spop(final String key, final long count) {
-    return new JedisClusterCommand<Set<String>>(connectionHandler, timeout, maxRedirections) {
+    return new JedisClusterCommand<Set<String>>(connectionHandler, maxRedirections) {


```