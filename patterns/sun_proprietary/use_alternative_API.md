---
layout: page
---
## openmrs/openmrs-core 2684.2

### Warning Message

---------------------

```java
/home/travis/build/openmrs/openmrs-core/api/sre/main/java/org/openmrs/utilMemoryleakutil.java:[20,23]kepAlivecache is internal prorietary API and may be removed in a future release

```

### Code Change

---------------------

***vespa-http-client/src/main/java/com/yahoo/vespa/http/client/runner/CommandLineArguments.java***

```diff
- import sun.net.www.http.KeepAliveCache;
+ import org.jboss.util.TimedCachePolicy;
```