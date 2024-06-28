---
layout: page
---
## jcabi/jcabi-github  903.3

### Warning Message

---------------------

```java
[WARNING]Cannot find annotation method 'message()'in type 'javax.validation.constraints.NotNul1':
class file for javax.validation.constraints.NotNull not found

```

### Code Change

---------------------

***src/main/java/com/jcabi/github/Assignees.java***

```diff
   import java.io.IOException;
-  import javax.validation.constraints.NotNull;
```