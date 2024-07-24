---
layout: page
---
## UniversalMediaServer/UniversalMediaServer 4572.3

### Warning Message

---------------------

```java
IMARNTNG]/home/travis/build/UniversaUMediaServer/UniversaUMediaServer/src/main/java/net/pms/configuration/Rendererconfiguration.java:[393,383
[unchecked]unchecked conversion
required:ArrayList<RendererConfiguration>
found:ArrayList

```

### Code Change

---------------------

***vespa-http-client/src/main/java/com/yahoo/vespa/http/client/runner/CommandLineArguments.java***

```diff
-        <arg>-Xlint:all,-options,-path</arg>
```