---
layout: page
---
## grails/grails-core 3031.1

### Error Message

---------------------

```java
/home/travis/build/grails/grails-core/grails-core/src/main/groovy/org/grails/transaction/ChainedTransactionManagerPostProcessor.java:188: error: ';' expected
                transactional = false
                                     ^
```

### Code Change

---------------------

***grails-core/grails-core/src/main/groovy/org/grails/transaction/ChainedTransactionManagerPostProcessor.java***

```diff
 if (isReadOnly != null && isReadOnly == true) {
-               transactional = false
+               transactional = false;
            }
```