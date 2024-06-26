---
layout: page
---
## ForgeEssentials/ForgeEssentials 383.1

### Error Message

---------------------

```java
/home/travis/build/ForgeEssentials/ForgeEssentialsMain/build/sources/java/com/forgeessentials/economy/network/S4PacketEconomy.java:33: error: method writeInt in class ByteBuf cannot be applied to given types; 
buf.writeInt(APIRegistry.wallet.getWallet(player)); 
^ 
required: int 
found: long 
reason: actual argument long cannot be converted to int by method invocation conversion 
```

### Code Change

---------------------

***src/main/java/com/forgeessentials/economy/network/S4PacketEconomy.java***

```diff
    @Override public void toBytes(ByteBuf buf)
    {
-        buf.writeInt(APIRegistry.wallet.getWallet(player));
+        buf.writeLong(APIRegistry.wallet.getWallet(player));
    }
```