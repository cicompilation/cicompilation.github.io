---
layout: page
---
## SpongePowered/SpongeAPI 5572.1

### Error Message

---------------------

```java
:compileJava/home/travis/build/SpongePowered/SpongeAPI/src/main/java/org/spongepowered/api/data/merge/MergeFunction.java:93: error: incompatible types: invalid functional descriptor for lambda expression 
return (a, b) -> that.merge(self.merge(a, b), b); 
^ 
method <C>(C,C)C in interface MergeFunction is generic 
where C is a type-variable: 
C extends ValueContainer<?> declared in method <C>merge(C,C) 
```

### Code Change

---------------------

***graylog2-server/src/main/java/org/graylog2/CommandLineArguments.java***

```diff
    default MergeFunction andThen(final MergeFunction that) {
        final MergeFunction self = this;
-       return (a, b) -> that.merge(self.merge(a, b), b);
        return new MergeFunction() {
            @Override
            public <C extends ValueContainer<?>> C merge(C original, C replacement) {
                 return that.merge(self.merge(original, replacement), replacement);
             }
         };
     }
```