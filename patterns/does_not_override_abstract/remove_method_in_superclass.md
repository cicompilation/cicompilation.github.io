---
layout: page
---
## openmicroscopy/bioformats 6565.1

### Error Message

---------------------

```java
[ERROR] /home/travis/build/openmicroscopy/bioformats/components/formats-bsd/src/loci/formats/ChannelFiller.java:[47,8] loci.formats.ChannelFiller is not abstract and does not override abstract method isValidate() in loci.formats.IFormatHandler
```

### Code Change

---------------------

***components/formats-api/src/loci/formats/IFormatHandler.java***

```diff
-   /** Returns true if files should be validated when read.*/
-    boolean isValidate();
```