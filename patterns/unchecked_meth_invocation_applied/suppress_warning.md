---
layout: page
---
## recommenders/rival  150.1

### Warning Message

---------------------

```java
[WARNING]/home/travis/build/recommenders/rival/rival-evaluate/src/test/java/net/recommenders/rival/evaluation/statistics/StatisticsTest.java:[96,77][unchecked]unchecked method invocation:method getConfidenceInterval in class ConfidenceInterval is applied to given types

```

### Code Change

---------------------

***...atform-base/src/main/java/org/gradle/platform/base/internal/DefaultPlatformContainer.java***

```diff
+   @SuppressWarnings("unchecked")
    @Test
    public void testConfidenceInterval2() {
```