---
layout: page
---
## scalecube/scalecube 2618.1

### Warning Message

---------------------

```java
/home/travis/build/scalecube/scalecube/transport/src/main/java/io/scalecube/transport/RecyclableLinkedBuffer.java:[61,21]
unchecked method invocation:method recycle in
class io.netty.util.Recycler is applied to given types
required:T,io.netty.util.Recycler.Handle<T>
found:io.scalecube.transport.RecyclableLinkedBuffer,io.netty.util.Recycler.Handle

```

### Code Change

---------------------

***.travis.yml***

```diff
  #remove this when done: {
+ install: true 
```