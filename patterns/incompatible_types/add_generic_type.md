---
layout: page
---
## geotools/geotools 2517.1

### Error Message

---------------------

```java
[ERROR] /home/travis/build/geotools/geotools/modules/unsupported/css/src/main/java/org/geotools/styling/css/DomainCoverage.java:[380,69] error: incompatible types: cannot infer type arguments for NumberRange<> 
```

### Code Change

---------------------

***app/src/main/java/com/fastaccess/ui/modules/feeds/FeedsFragment.java***

```diff
        if (!merged) {
-           scaleDependentFilters.add(new SLDSelector(new NumberRange<>(range), filter));
+           scaleDependentFilters.add(new SLDSelector(new NumberRange<Double>(range), filter));
        }
```