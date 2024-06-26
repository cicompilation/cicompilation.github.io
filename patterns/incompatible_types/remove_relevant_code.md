---
layout: page
---
## beecloud/beecloud-java 442.1

### Error Message

---------------------

```java
[ERROR] /home/travis/build/beecloud/beecloud-java/sdk/src/main/java/cn/beecloud/BCPay.java:[1078,41] incompatible types 
found : java.lang.String 
required: java.util.Map<java.lang.String,java.lang.Object> 
```

### Code Change

---------------------

***sdk/src/main/java/cn/beecloud/BCPay.java***

```diff
-        List<String> bankList = new ArrayList<String>();
-        for (Map<String, Object> bill : bills) {
-            BCOrder bcOrder = new BCOrder();
-            generateBCOrderBean(bill, bcOrder);
-            bcOrderList.add(bcOrder);
-        }
-        return bcOrderList;
```