---
layout: page
---
## st-js/st-js  11.2

### Warning Message

---------------------

```java
[WARNING]/home/travis/build/st-js/st-js/test-helper/src/main/java/org/stjs/testing/driver/TestResource.java:[22,32]FileURLConnection is internal proprietary API and may be removed in a future release
[INF0]

```

### Code Change

---------------------

***test-helper/src/main/java/org/stjs/testing/driver/TestResource.java***

```diff
  import com.sun.net.httpserver.HttpExchange;

- import sun.net.www.protocol.file.FileURLConnection;
```