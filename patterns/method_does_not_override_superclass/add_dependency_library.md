---
layout: page
---
## openzipkin/zipkin 5995.1

### Error Message

---------------------

```java
[ERROR] /home/travis/build/openzipkin/zipkin/zipkin-storage/cassandra3/src/test/java/zipkin/storage/cassandra3/integration/CassandraDependenciesTest.java:[40,3] method does not override or implement a method from a supertype 
```

### Code Change

---------------------

***pom.xml***

```diff
+    <dependency>
+       <groupId>io.zipkin.zipkin2</groupId>
+       <artifactId>zipkin</artifactId>
+       <type>test-jar</type>
+       <version>${project.version}</version>
+     </dependency>

```

***zipkin-autoconfigure/storage-cassandra3/pom.xml***
```diff
+<dependency>
+     <groupId>${project.groupId}</groupId>
+     <artifactId>zipkin</artifactId>
+   </dependency>
```

