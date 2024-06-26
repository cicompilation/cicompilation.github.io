---
layout: page
---
## MinecraftForge/MinecraftForge 2338.1

### Error Message

---------------------

```java
/home/travis/build/MinecraftForge/MinecraftForge/src/main/java/net/minecraftforge/server/command/CommandTps.java:72: error: no suitable method found for getIntIDs(no arguments)
            for (Integer dimId : DimensionManager.getIntIDs())
                                                 ^
    method DimensionManager.getIntIDs(Collection<ResourceLocation>) is not applicable
      (actual and formal argument lists differ in length)
    method DimensionManager.getIntIDs(boolean) is not applicable
      (actual and formal argument lists differ in length)
```

### Code Change

---------------------

***src/main/java/net/minecraftforge/common/DimensionManager.java***

```diff
+    public static Set<Integer> getIntIDs()
+     {
+         Set<ResourceLocation> ids = getIDs();
+         return getIntIDs(ids);
+     }
  
```