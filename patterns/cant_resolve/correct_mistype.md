---
layout: page
---
## openMF/mifos-mobile 530.1

### Error Message

---------------------

```java
/home/travis/build/openMF/self-service-app/app/src/main/java/org/mifos/selfserviceapp/ui/activities/HomeActivity.java:314: error: cannot find symbol
                        } else if (fragment instanceof HelpUCFragment) {
                                                       ^
  symbol: class HelpUCFragment
```

### Code Change

---------------------

***app/src/main/java/org/mifos/selfserviceapp/ui/activities/HomeActivity.java***

```diff
            setNavigationViewSelectedItem(R.id.item_beneficiaries);
-        } else if (fragment instanceof HelpUCFragment) {
+        } else if (fragment instanceof HelpFragment) {
            setNavigationViewSelectedItem(R.id.item_help);
```