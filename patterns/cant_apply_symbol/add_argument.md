---
layout: page
---
## azkaban/azkaban 3004.1

### Error Message

---------------------

```java
/home/travis/build/azkaban/azkaban/azkaban-common/src/test/java/azkaban/project/FlowTriggerTest.java:39: error: constructor FlowTriggerDependency in class FlowTriggerDependency cannot be applied to given types; 
final FlowTriggerDependency dep = new FlowTriggerDependency(depProps); 
^ 
required: String,String,Props 
found: Props 
reason: actual and formal argument lists differ in length 
```

### Code Change

---------------------

***azkaban-common/src/test/java/azkaban/project/FlowTriggerTest.java***

```diff
  private FlowTriggerDependency createTestDependency(final String type, final String name) {
     final Props depProps = new Props();
-    depProps.put(Constants.DependencyProperties.DEPENDENCY_NAME, name);
-    depProps.put(Constants.DependencyProperties.DEPENDENCY_TYPE, type);
-    final FlowTriggerDependency dep = new FlowTriggerDependency(depProps);
+     final FlowTriggerDependency dep = new FlowTriggerDependency(name, type, depProps);
     return dep;
   }
```