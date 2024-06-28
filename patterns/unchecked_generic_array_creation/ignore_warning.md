---
layout: page
---
## gephi/gephi 16.1

### Warning Message

---------------------

```java
home/trvis/build/gehi/gephi/nouesPreviewtxportuIsre/main/java/or/gephi/ui/exporter/preview/UIExorterPNGPanel.jav:192,17 [unchecked]unchecked gneric aray creation for varargs parameter of type Validator<String>[]

```

### Code Change

---------------------

***pom.xml***

```diff
+               <gephi.javac.xlint>-Xlint:none</gephi.javac.xlint>
            </properties>
```