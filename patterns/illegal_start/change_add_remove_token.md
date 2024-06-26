---
layout: page
---
## wicketstuff/core 388.1

### Error Message

---------------------

```java
 /home/travis/build/wicketstuff/core/datastores-parent/datastore-redis/src/main/java/org/wicketstuff/datastores/redis/RedisDataStore.java:[151,1] error: illegal start of expression 
```

### Code Change

---------------------

***datastores-parent/datastore-redis/src/main/java/org/wicketstuff/datastores/redis/RedisDataStore.java***

```diff
			if (settings.getRecordTtl() != null) {
				resource.expire(key, (int) settings.getRecordTtl().seconds());
+		  }
		} finally {
			jedisPool.returnResource(resource);
		}
```