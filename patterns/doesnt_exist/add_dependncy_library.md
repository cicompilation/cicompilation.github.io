---
layout: page
---
## orbit/orbit 783.1

### Error Message

---------------------

```java
[ERROR] /home/travis/build/orbit/orbit/actors/test/actor-tests/src/main/java/cloud/orbit/actors/test/FakeGroup.java:[40,42] package com.github.benmanes.caffeine.cache does not exist 
```

### Code Change

---------------------

***actors/test/actor-tests/pom.xml***

```diff
            <version>1.7.21</version>
        </dependency>
+        <dependency>
+            <groupId>com.github.ben-manes.caffeine</groupId>
+            <artifactId>caffeine</artifactId>
+            <version>2.3.0</version>
+        </dependency>
    </dependencies>
</project>
```