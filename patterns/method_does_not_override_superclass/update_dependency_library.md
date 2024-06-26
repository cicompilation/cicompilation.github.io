---
layout: page
---
## Graylog2/graylog2-server 260.1

### Error Message

---------------------

```java
[ERROR] /home/travis/builds/Graylog2/graylog2-server/src/main/java/org/graylog2/outputs/ElasticSearchOutput.java:[49,4] error: method does not override or implement a method from a supertype
```

### Code Change

---------------------

***pom.xml***

```diff
 <dependency>
            <groupId>org.graylog2</groupId>
            <artifactId>graylog2-plugin</artifactId>
-           <version>0.9.7.7</version>
+           <version>0.9.7.8</version>
        </dependency>
    </dependencies>
```

