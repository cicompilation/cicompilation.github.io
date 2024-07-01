---
layout: page
---
## INRIA/spoon 5102.1

### Warning Message

---------------------

```java
bootstrap class path not set in conjunction with -source 1.8
```

### Code Change

---------------------

***chore/travis/travis-jdk9-other-seed.sh → chore/travis/travis-jdk8-other-seed.sh***

```diff
-    jdk_switcher use oraclejdk9 && SPOON_SEED_CU_COMPARATOR=$(( ( RANDOM )  + 1 )) mvn -Djava.src.version=1.9 test
+    jdk_switcher use oraclejdk8 && SPOON_SEED_CU_COMPARATOR=1 mvn -Djava.src.version=1.8 test
```