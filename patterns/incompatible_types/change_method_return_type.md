---
layout: page
---
## graphaware/neo4j-nlp 65.1

### Error Message

---------------------

```java
[ERROR] /home/travis/build/graphaware/neo4j-nlp/src/main/java/com/graphaware/nlp/NLPManager.java:[200,42] incompatible types: java.util.Map<java.lang.String,java.lang.Boolean> cannot be converted to java.util.Map<java.lang.String,java.lang.Object> 
```

### Code Change

---------------------

***src/main/java/com/graphaware/nlp/processor/PipelineInfo.java***

```diff
-   public Map<String, Object> getSpecifications() {
+   public Map<String, Boolean> getSpecifications() {
         return specifications;
    }
```