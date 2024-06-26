---
layout: page
---
## junit-team/junit5 734.1

### Error Message

---------------------

```java
:junit5-engine:compileJava/home/travis/build/junit-team/junit-lambda/junit5-engine/src/main/java/org/junit/gen5/engine/junit5/descriptor/ClassBasedContainerExtensionContext.java:19: error: ClassBasedContainerExtensionContext is not abstract and does not override abstract method publishReportEntry(Map<String,String>) in ExtensionContext

final class ClassBasedContainerExtensionContext extends AbstractExtensionContext implements ContainerExtensionContext {

        ^
```

### Code Change

---------------------

***src/main/java/org/junit/gen5/engine/junit5/descriptor/AbstractExtensionContext.java***

```diff
+ 	public void publishReportEntry(Map<String, String> entry) {
+ 		engineExecutionContext.publishReportEntry(this.getTestDescriptor(), entry);
  	}
```