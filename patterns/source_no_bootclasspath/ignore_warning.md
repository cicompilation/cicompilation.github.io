---
layout: page
---
## bndtools/bnd 2773.2

### Warning Message

---------------------

```java
compileJavawarning:[options]bootstrap class path not set in conjunction with -source 1.7
```

### Code Change

---------------------

***build.gradle***

```diff
- options.compilerArgs.add('-Xlint:-options')
```