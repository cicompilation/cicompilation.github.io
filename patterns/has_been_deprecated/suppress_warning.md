---
layout: page
---
## SpongePowered/SpongeCommon 884.4

### Warning Message

---------------------

```java
/home/travis/build/SpongePowered/SpongeCommon/build/sources/java/org/spongepowered/common/data/processor/value/tileentity/SignLinesValueProcessor.java:87:warning:[deprecation] legacy() in Texts has been deprecated
```

### Code Change

---------------------

***...ava/org/spongepowered/common/data/processor/value/tileentity/SignLinesValueProcessor.java***

```diff
 import java.util.List;

+@SuppressWarnings("deprecation")
 public class SignLinesValueProcessor implements ValueProcessor<List<Text>, ListValue<Text>> {
```