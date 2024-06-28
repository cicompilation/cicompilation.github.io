---
layout: page
---
## JabRef/jabref 346.1

### Warning Message

---------------------

```java
:compileJava/home/travis/build/JabRef/jabref/src/main/gen/net/sf/jabref/search/SearchExpressionLexer.java:45:warning:[unchecked] unchecked call to put(K,V)as a member of theraw type java.util.Hashtable
literals.put(new ANTLRHashString("matches",this),new Integer(8));
^
```

### Code Change

---------------------

***vespa-http-client/src/main/java/com/yahoo/vespa/http/client/runner/CommandLineArguments.java***

```diff
     options.encoding = 'UTF-8'
-    options.compilerArgs << "-Xlint:unchecked"
+    options.compilerArgs << "-Xlint:none"
```