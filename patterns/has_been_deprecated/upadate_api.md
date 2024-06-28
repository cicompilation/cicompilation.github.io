---
layout: page
---
## vespa-engine/vespa 5950.1

### Warning Message

---------------------

```java
/source/vespa-http-client/src/main/java/com/yahoo/vespa/http/client/runner/CommandLineArguments.java:[211,91] ALLOW_ALL_HOSTNAME_VERIFIER in org.apache.http.conn.ssl.SSLConnectionSocketFactory has been deprecated
```

### Code Change

---------------------

***vespa-http-client/src/main/java/com/yahoo/vespa/http/client/runner/CommandLineArguments.java
***

```diff
    new ConnectionParams.Builder()
-            .setHostnameVerifier(insecure ? SSLConnectionSocketFactory.ALLOW_ALL_HOSTNAME_VERIFIER :
+            .setHostnameVerifier(insecure ? NoopHostnameVerifier.INSTANCE :
```