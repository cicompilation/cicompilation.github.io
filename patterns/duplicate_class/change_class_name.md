---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: page
---
## Texera/texera 13.1

### Error Message

---------------------

```java
[ERROR] /home/travis/build/TextDB/textdb/textdb/textdb-sandbox/src/main/java/edu/uci/ics/textdb/sandbox/DummyHelloWorld.java:[7,8]
duplicate class: edu.uci.ics.textdb.sandbox.DummyHelloWorld 
```

### Code Change

---------------------

***textdb/textdb-sandbox/src/main/java/edu/uci/ics/textdb/sandbox/ZuozhiHelloWorld.java***

```diff
- public class DummyHelloWorld
+ public class ZuozhiHelloWorld
  {
      public static void main( String[] args )
```