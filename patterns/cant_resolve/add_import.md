---
layout: page
---
## naver/pinpoint 164.1

### Error Message

---------------------

```java
[ERROR] /home/travis/build/naver/pinpoint/web/src/main/java/com/navercorp/pinpoint/web/service/TransactionInfoServiceImpl.java:[73,5] cannot find symbol 
symbol : class Value 
location: class com.navercorp.pinpoint.web.service.TransactionInfoServiceImpl 
```

### Code Change

---------------------

***web/src/main/java/com/navercorp/pinpoint/web/service/TransactionInfoServiceImpl.java***

```diff
  import org.springframework.beans.factory.annotation.Autowired;
+ import org.springframework.beans.factory.annotation.Value;
  import org.springframework.stereotype.Service;
```