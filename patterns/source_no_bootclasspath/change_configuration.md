---
layout: page
---
## SpoutDev/Spout  10.1

### Warning Message

---------------------

```java
[WARNING]bootstrap class path not set in conjunction with -source 1.6

```

### Code Change

---------------------

***pom.xml***

```diff
-    <source>1.6</source>
-    <target>1.6</target>
+    <source>1.7</source>
+    <target>1.7</target>
```