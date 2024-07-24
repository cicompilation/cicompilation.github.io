---
layout: page
---
## HPI-Information-Systems/Metanome  1642.2

### Warning Message

---------------------

```java
[WARNING] /home/travis/build/HPI-Information-Systems/Metanome/backend/src/test/java/de/metanome/backend/configuration/DefaultConfigurationFactoryTest.java:[165,5] assertEquals(java.lang.Object[],java.lang.Object[]) in org.junit.Assert has been deprecated

```

### Code Change

---------------------

***backend/src/test/java/de/metanome/backend/configuration/DefaultConfigurationFactoryTest.java***

```diff
-    assertEquals(possibleValues, actualConfigValue.values[0]);
```