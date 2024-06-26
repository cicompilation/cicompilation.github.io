---
layout: page
---
## Graylog2/graylog2-server 723.1

### Error Message

---------------------

```java
[ERROR] /home/travis/build/Graylog2/graylog2-server/graylog2-server/src/main/java/org/graylog2/CommandLineArguments.java:[45,40] incompatible types 
required: java.lang.String 
found: org.graylog2.Version
```

### Code Change

---------------------

***graylog2-server/src/main/java/org/graylog2/CommandLineArguments.java***

```diff
     @Parameter(names = {"-v", "--plugin-version"}, description = "Install plugin with this version")
-    private String pluginVersion = Core.GRAYLOG2_VERSION;
+    private String pluginVersion = Core.GRAYLOG2_VERSION.toString();
```