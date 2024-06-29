---
layout: page
---
## SamirTalwar/Rekord 100.1

### Warning Message

---------------------

```java
[WARNING] /home/travis/build/SamirTalwar/Rekord/validation/src/main/java/com/noodlesandwich/rekord/validation/RekordMatchers.java:[61,66] Varargs method could cause heap pollution from non-reifiable varargs parameter keys
```

### Code Change

---------------------

***...atform-base/src/main/java/org/gradle/platform/base/internal/DefaultPlatformContainer.java***

```diff
+   @SafeVarargs
    public static <T> Matcher<FixedRekord<T>> hasProperties(final Key<T, ?>... keys) {
```