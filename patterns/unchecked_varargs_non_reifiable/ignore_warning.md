---
layout: page
---
## GoogleCloudPlatform/DataflowJavaSDK  1.2

### Warning Message

---------------------

```java
[WARNING] /home/travis/build/GoogleCloudPlatform/DataflowJavaSDK/sdk/src/main/java/com/google/cloud/dataflow/sdk/testing/DataflowAssert.java:[218,54] Possible heap pollution from parameterized vararg type T
^
```

### Code Change

---------------------

***pom.xml***

```diff
+         <arg>-Xlint:-unchecked</arg>
+         <arg>-Xlint:-varargs</arg>
```