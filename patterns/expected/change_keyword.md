---
layout: page
---
## openmicroscopy/bioformats 6073.1

### Error Message

---------------------

```java
[ERROR]/home/travis/build/openmicroscopy/bioformats/components/formats-bsd/src/loci/formats/in/FakeReader.java:[893,37] ')' expected 
```

### Code Change

---------------------

***components/formats-bsd/src/loci/formats/in/FakeReader.java***

```diff
-store.setEllipseRadiusX(nefw Double(5.0), roiCount, 0);
+store.setEllipseRadiusX(new Double(5.0), roiCount, 0);
```