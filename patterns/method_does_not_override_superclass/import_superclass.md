---
layout: page
---
## xetorthio/jedis 717.1


### Error Message

---------------------

```java
[ERROR] /home/travis/build/xetorthio/jedis/src/main/java/redis/clients/jedis/JedisSentinelPool.java:[177,3] method does not override or implement a method from a supertype 
```

### Code Change

---------------------

***src/main/java/redis/clients/jedis/JedisSentinelPool.java***

```diff
 import redis.clients.jedis.exceptions.JedisConnectionException;
 import redis.clients.jedis.exceptions.JedisException;
+import redis.clients.util.Pool;   
...
 @Override
   public Jedis getResource() {
     while (true) {
       Jedis jedis = super.getResource();
       jedis.setDataSource(this);
```