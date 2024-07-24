---
layout: page
---
## SamirTalwar/Rekord 100.1

### Warning Message

---------------------

```java
[WARNING] /home/travis/build/SamirTalwar/Rekord/validation/src/main/java/com/noodlesandwich/rekord/validation/RekordMatchers.java:[60,80] Possible heap polution from parameterized vararg type com.noodlesandwich.rekord.keys.Key<T,?>

```

### Code Change

---------------------

***...atform-base/src/main/java/org/gradle/platform/base/internal/DefaultPlatformContainer.java***

```diff
+   @SafeVarargs
    public static <T> Matcher<FixedRekord<T>> hasProperties(final Key<T, ?>... keys) {
```