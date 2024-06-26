---
layout: page
---
## Unidata/thredds 754.1

### Error Message

---------------------

```java
[ERROR] /home/travis/build/Unidata/thredds/cdm/src/main/java/ucar/nc2/stream/CdmRemote.java:93: error: cannot find symbol 
private HTTPSession httpClient; 
^ 
symbol: class HTTPSession 
location: class CdmRemote 
```

### Code Change

---------------------

***cdm/build.gradle***

```diff
  dependencies {
    compile project(':udunits')
+   compile project(':httpclient')
    compile ('org.apache.httpcomponents:httpcore:4.2.5', 'org.apache.httpcomponents:httpclient:4.2.6', 'org.apache.httpcomponents:httpmime:4.2.6')
    compile 'com.google.protobuf:protobuf-java:2.5.0'
    compile 'joda-time:joda-time:2.2'
```