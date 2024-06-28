---
layout: page
---
## apache/accumulo 389.1

### Warning Message

---------------------

```java
/home/travis/build/apache/accunulo/minicuster/sre/main/java/org/apache/accumlo/minicuster/impl/MiniAcumulocustercontrol.java:[137,10]unchecked method invocation: method start in class org.apache.accumulo.minicluster.impl.MiniAccumuloclustercontrol is applied to given types
required:org.apache.accumulo.minicluster.ServerType,java.lang.String,java.util.Map<java.lang.String,java.lang.String>,int
found:org.apache.accumulo.minicluster.ServerType,java.lang.String,java.util.Map,int

```

### Code Change

---------------------

***...luster/src/main/java/org/apache/accumulo/minicluster/impl/MiniAccumuloClusterControl.java***

```diff
  public synchronized void start(ServerType server, String hostname) throws IOException {
-    start(server, hostname, Collections.EMPTY_MAP, Integer.MAX_VALUE);
+    start(server, hostname, Collections.<String,String> emptyMap(), Integer.MAX_VALUE);
  }
```