---
layout: page
---
## square/okhttp 6999.1

### Error Message

---------------------

```java
[ERROR] /home/travis/build/square/okhttp/samples/guide/src/main/java/okhttp3/recipes/WebSocketEcho.java:[61,3] method does not override or implement a method from a supertype 
```

### Code Change

---------------------

***samples/guide/src/main/java/okhttp3/recipes/WebSocketEcho.java***

```diff
-   @Override public void onPong(Buffer payload) {
-   System.out.println("PONG: " + payload.readUtf8());
+   @Override public void onPong(ByteString payload) {
+   System.out.println("PONG: " + payload.utf8());
  }
```