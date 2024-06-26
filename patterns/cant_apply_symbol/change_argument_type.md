---
layout: page
---
## openmicroscopy/bioformats 2951.1

### Error Message

---------------------

```java
[ERROR] /home/travis/build/openmicroscopy/bioformats/components/formats-gpl/src/loci/formats/in/NativeND2Reader.java:[1674,34] no suitable method found for add(int) 
method java.util.AbstractCollection.add(java.lang.Double) is not applicable 
(argument mismatch; int cannot be converted to java.lang.Double) 
method java.util.AbstractList.add(java.lang.Double) is not applicable 
(argument mismatch; int cannot be converted to java.lang.Double) 
method java.util.ArrayList.add(java.lang.Double) is not applicable 
(argument mismatch; int cannot be converted to java.lang.Double) 
```

### Code Change

---------------------

***components/formats-gpl/src/loci/formats/in/NativeND2Reader.java***

```diff
        else if (name.equals("EmWavelength")) {
           Double wave = Double.parseDouble(value.toString());
-          textEmissionWavelengths.add(wave.intValue());
+          textEmissionWavelengths.add(wave);
         }
```