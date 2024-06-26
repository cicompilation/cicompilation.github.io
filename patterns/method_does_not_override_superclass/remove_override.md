---
layout: page
---
## pircbotx/pircbotx 100.1


### Error Message

---------------------

```java
[ERROR] /home/travis/build/[secure]/pircbotx/src/main/java/org/pircbotx/hooks/events/UnknownEvent.java:[45,9] method does not override or implement a method from a supertype 
```

### Code Change

---------------------

***src/main/java/org/pircbotx/hooks/events/UnknownEvent.java***

```diff
-    @Getter(onMethod = @_(
-			@Override))
+	@Getter
	protected final String target;
	/**
	 * The nickname (if any) of the originating user
	 */
```