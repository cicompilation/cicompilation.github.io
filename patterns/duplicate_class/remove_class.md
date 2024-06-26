---
layout: page
---
## mongodb/mongo-java-driver 2274.1

### Error Message

---------------------

```java
/home/travis/build/mongodb/mongo-java-driver/bson/src/main/org/bson/codecs/DocumentCodecProvider.java:32: error: duplicate class: org.bson.codecs.DocumentCodecProvider 
public class DocumentCodecProvider implements CodecProvider { 
^ 
```

### Code Change

---------------------

***bson/src/main/org/bson/codecs/MapCodecProvider.java***

```diff
- package org.bson.codecs;
-  import org.bson.Document;
- import org.bson.Transformer;
- import org.bson.codecs.configuration.CodecProvider;
- import org.bson.codecs.configuration.CodecRegistry;
- import org.bson.types.CodeWithScope;
-  import static org.bson.assertions.Assertions.notNull;
- /**
-  * A {@code CodecProvider} for the Document class and all the default Codec implementations on which it depends.
-  *
-  * @since 3.0
-  */
- public class DocumentCodecProvider implements CodecProvider {
-     private final BsonTypeClassMap bsonTypeClassMap;
-     private final Transformer valueTransformer;
```