---
layout: page
---
## naver/pinpoint 714.1

### Error Message

---------------------

```java
/home/travis/build/naver/pinpoint/collector/src/main/java/com/navercorp/pinpoint/collector/dao/hbase/HbaseSqlMetaDataDao.java:[67,33] error: cannot find symbol 
symbol: variable SQL_METADATA_VER2_CF_SQL 
location: class HBaseTables 
```

### Code Change

---------------------

*** commons-hbase/src/main/java/com/navercorp/pinpoint/common/hbase/HBaseTables.java***

```diff
 public static final byte[] SQL_METADATA_CF_SQL = Bytes.toBytes("Sql");
    
+public static final String SQL_METADATA_VER2 = "SqlMetaData_Ver2";
+public static final byte[] SQL_METADATA_VER2_CF_SQL = Bytes.toBytes("Sql");

```