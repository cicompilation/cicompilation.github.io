---
layout: page
---
## LapisBlue/Pore  29.2

### Warning Message

---------------------

```java
/home/travis/build/LapisBlue/Pore/src/main/java/net/amigocraft/pore/implementation/PoreUnsafeValues.java:7:warning:[deprecation]UnsafeValues in org.bukkit has been deprecated
```

### Code Change

---------------------

***build.gradle***

```diff
tasks.withType(JavaCompile) {
     options.encoding = 'UTF-8'
-    options.deprecation = true
}
```