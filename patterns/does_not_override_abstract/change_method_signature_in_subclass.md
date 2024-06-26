---
layout: page
---
## xiongbeer/Cobweb 154.1

### Error Message

---------------------

```java
[ERROR] /home/travis/build/xiongbeer/WebVeins/src/main/java/com/xiongbeer/cobweb/zk/resources/INodeDirectory.java:[10,8] com.xiongbeer.cobweb.zk.resources.INodeDirectory is not abstract and does not override abstract method getPath() in com.xiongbeer.cobweb.zk.resources.INodeAttributes 
```

### Code Change

---------------------

***src/main/java/com/xiongbeer/cobweb/zk/resources/INodeDirectory.java***

```diff
-     public Path getPath() {
+     public String getPath() {
          return null;
      }
```