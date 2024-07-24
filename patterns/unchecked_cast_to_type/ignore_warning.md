---
layout: page
---
## oblac/jodd 1188.1

### Warning Message

---------------------

```java
/home/travis/build/oblac/jodd/jodd-core/src/main/java/jodd/io/findfile/FindFile.java:653: warning: [unchecked] unchecked cast
pathListOriginal = (LinkedList<File>) pathList.clone();
^
required: LinkedList<File>
found: Object
```

### Code Change

---------------------

***build.gradle***

```diff
		options.compilerArgs << "-Xlint:-options"
-		options.compilerArgs << "-Xlint:unchecked" << "-Xlint:deprecation"
```