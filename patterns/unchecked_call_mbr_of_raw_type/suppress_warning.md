---
layout: page
---
## yahoo/omid 244.1

### Warning Message

---------------------

```java
/home/travis/build/yaho/omid/comon/sre/main/java/con/yahoo/omid/YAMLUtits.java:156,341 unchecked call to putAll(java.uti1.Maps?extends K,? extends V>)as a member of the raw type java.util.Map

```

### Code Change

---------------------

***...atform-base/src/main/java/org/gradle/platform/base/internal/DefaultPlatformContainer.java***

```diff
+   @SuppressWarnings("unchecked")
    private Map loadSettings(String resourcePath, String defaultResourcePath) throws IOException {
        Map defaultSetting = loadAsMap(defaultResourcePath);
```