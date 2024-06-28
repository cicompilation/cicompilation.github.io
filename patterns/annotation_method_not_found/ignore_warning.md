---
layout: page
---
## cloudfoundry/uaa 1405.1

### Warning Message

---------------------

```java
:cloudfoundry-identity-comon:compileJava/home/travis/.gradle/caches/modules-2/files-2.1/org.springframework.security.oauth/spring-security-oauth2/2.0.3.RELEASE/4087aa209f8d73576bd08f1e3ed395da43e7dc79/spring-security-oauth2-
2.0.3.RELEASE.jar(org/springframeworksecurity/oauth2/como/OAuth2AcessToken.class):warning:Cannot find anotation method 'using()'in type JsonSerialize': class file for com.fasterxml.jackson.databind.annotation.JsonSerialize not found
```

### Code Change

---------------------

***.travis.yml***

```diff
   apply plugin: 'java'
+  [compileJava, compileTestJava]*.options*.compilerArgs = ['-Xlint:none']
```