---
layout: page
---
## vespa-engine/vespa 5950.1

### Warning Message

---------------------

```java
:logback-android:compileDebugJavaWithJavac/home/travis/build/tony19/logback-android/logback-
android/src/main/java/ch/qos/logback/core/rolling/helper/FileNamepattern.java:89:warning:[unchecked] unchecked conversion 
DateTokenConverter<0bject> dtc =(DateTokenConverter)p;
required:DateTokenConverter<0bject>
found:DateTokenConverter
```

### Code Change

---------------------

***logback-android/src/main/java/ch/qos/logback/core/rolling/helper/FileNamePattern.java***

```diff
      if (p instanceof DateTokenConverter) {
-        DateTokenConverter<Object> dtc = (DateTokenConverter) p;
+        DateTokenConverter<Object> dtc = (DateTokenConverter<Object>) p;
```