---
layout: page
---
## oblac/jodd 1188.1

### Warning Message

---------------------

```java
/home/travis/buitd/oblac/jod/iod-bea/sre/main/java/jodd/bean/BeantilBean.java:361:warning Unchecken unchecked method invocation

```

### Code Change

---------------------

***build.gradle***

```diff
		options.compilerArgs << "-Xlint:-options"
-		options.compilerArgs << "-Xlint:unchecked" << "-Xlint:deprecation"
```