---
layout: page
---
## shivam-maharshi/algorithms 105.1

### Error Message

---------------------

```java
/home/travis/build/shivam-maharshi/algorithms/src/main/java/pramp/Interview10.java:1: error: duplicate class: Pramp 
class Pramp { 
^ 
```

### Code Change

---------------------

***src/main/java/pramp/Interview10.java***

```diff
- class Pramp {
+ package pramp;
+ public class Interview10 {
```