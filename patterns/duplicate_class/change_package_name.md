---
layout: page
---
## fivesmallq/web-data-extractor 152.1

### Error Message

---------------------

```java
[ERROR] /home/travis/build/fivesmallq/web-data-extractor/src/main/java/im/nll/data/extractor/utils/Reflect.java:[62,8] duplicate class: org.joor.Reflect
```

### Code Change

---------------------

***src/main/java/im/nll/data/extractor/utils/Reflect.java***

```diff
- package org.joor;
+ package im.nll.data.extractor.utils;
  import im.nll.data.extractor.exception.ReflectException;
  import java.lang.reflect.*;
```