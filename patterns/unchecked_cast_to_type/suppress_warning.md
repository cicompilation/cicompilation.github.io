---
layout: page
---
## gradle/gradle  1755.1

### Warning Message

---------------------

```java
pDlatfornase:cmpileJava/hone/travis/build/gradle/gradle/subprojects/platform-base/src/min/java/or/gradle/platfora/base/internal/DefaultPlatforncontainer.ava:56:
warning:[unchecked]unchecked cast
selected.add((T)platform);
required:T
found:Platform
where T is a type-variable:
T extends Platform declared in method <T>select(Class<T>,List<String>)


```

### Code Change

---------------------

***...atform-base/src/main/java/org/gradle/platform/base/internal/DefaultPlatformContainer.java***

```diff
+   @SuppressWarnings("unchecked")
    public <T extends Platform> List<T> select(final Class<T> type, final List<String> targets) {
```