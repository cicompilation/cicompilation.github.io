---
layout: page
---
## guardianproject/haven 5.1

### Error Message

---------------------

```java
/home/travis/build/guardianproject/haven/src/main/java/org/havenapp/main/service/MonitorService.java:33: error: package info.guardianproject.phoneypot does not exist
import info.guardianproject.phoneypot.R;
                                     ^
```

### Code Change

---------------------

***src/main/java/org/havenapp/main/service/MonitorService.java***

```diff
- import info.guardianproject.phoneypot.R;
  import org.havenapp.main.PreferenceManager;
+ import org.havenapp.main.R;
```