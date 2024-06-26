---
layout: page
---
## cloudfoundry/uaa 5520.4

### Error Message

---------------------

```java
 /home/travis/build/cloudfoundry/uaa/uaa/src/test/java/org/cloudfoundry/identity/uaa/mock/clients/AdminClientCreator.java:25: error: cannot find symbol 
import static org.cloudfoundry.identity.uaa.mock.util.ClientDetailsHelper.clientFromString; 
^ 
symbol: class ClientDetailsHelper 
location: package org.cloudfoundry.identity.uaa.mock.util 
```

### Code Change

---------------------

***uaa/src/test/java/org/cloudfoundry/identity/uaa/mock/util/ClientDetailsHelper.java***

```diff
+package org.cloudfoundry.identity.uaa.mock.util;
+import org.cloudfoundry.identity.uaa.oauth.client.ClientDetailsModification;
+import org.cloudfoundry.identity.uaa.util.JsonUtils;
+import org.springframework.security.oauth2.provider.ClientDetails;
+public class ClientDetailsHelper {
+   public static Object fromString(String body, Class<?> clazz) throws Exception {
+       return JsonUtils.readValue(body, clazz);
+   }
+    public static ClientDetails[] clientArrayFromString(String clients) throws Exception {
+       return (ClientDetails[])arrayFromString(clients, ClientDetailsModification[].class);
+   }
+    public static Object[] arrayFromString(String body, Class<?> clazz) throws Exception {
+       return (Object[])JsonUtils.readValue(body, clazz);
+   }
+    public static ClientDetails clientFromString(String client) throws Exception {
+       return (ClientDetails)fromString(client, ClientDetailsModification.class);
+   }
+}

```