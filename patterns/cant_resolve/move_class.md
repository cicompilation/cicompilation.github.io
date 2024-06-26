---
layout: page
---
## azkaban/azkaban 1670.1

### Error Message

---------------------

```java
/home/travis/build/azkaban/azkaban/azkaban-common/src/test/java/azkaban/executor/ExecutorManagerTest.java:42: error: cannot find symbol 
private ExecutorManager manager; 
        ^ 
symbol: class ExecutorManager 
location: class ExecutorManagerTest 
```

### Code Change

---------------------

***azkaban/azkaban-web-server/src/test/java/azkaban/{executor->webapp}/ExecutorManagerTest.java***

```diff
- package azkaban.executor;
-
+ package azkaban.webapp;
+ import azkaban.executor.ExecutableFlow;
+ import azkaban.executor.ExecutionOptions;
+ import azkaban.executor.ExecutionReference;
+ import azkaban.executor.Executor;
+ import azkaban.executor.ExecutorLoader;
+ import azkaban.executor.ExecutorManagerException;
+ import azkaban.executor.MockExecutorLoader;
+ import azkaban.executor.Status; 

```