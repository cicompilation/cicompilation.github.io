---
layout: page
---
## zendesk/maxwell 1060.1

### Error Message

---------------------

```java
[ERROR] /home/travis/build/zendesk/maxwell/src/test/java/com/zendesk/maxwell/BootstrapIntegrationTest.java:[56,24] no suitable method found for getRowsForSQL(<nulltype>,java.lang.String[],<nulltype>,boolean) 
method com.zendesk.maxwell.AbstractMaxwellTest.getRowsForSQL(com.zendesk.maxwell.MaxwellFilter,java.lang.String[]) is not applicable 
(actual and formal argument lists differ in length) 
method com.zendesk.maxwell.AbstractMaxwellTest.getRowsForSQL(com.zendesk.maxwell.MaxwellFilter,java.lang.String[],java.lang.String[]) is not applicable 
(actual and formal argument lists differ in length) 
method com.zendesk.maxwell.AbstractMaxwellTest.getRowsForSQL(com.zendesk.maxwell.MysqlIsolatedServer,com.zendesk.maxwell.MaxwellFilter,java.lang.String[],java.lang.String[]) is not applicable 
(actual argument java.lang.String[] cannot be converted to com.zendesk.maxwell.MaxwellFilter by method invocation conversion) 
method com.zendesk.maxwell.AbstractMaxwellTest.getRowsForSQL(com.zendesk.maxwell.MysqlIsolatedServer,com.zendesk.maxwell.MaxwellFilter,java.lang.String[],java.lang.String[],boolean) is not applicable 
(actual and formal argument lists differ in length) 
```

### Code Change

---------------------

***src/test/java/com/zendesk/maxwell/BootstrapIntegrationTest.java***

```diff
- 	list = getRowsForSQL(null, input, null, false);
+		list = getRowsForSQL(null, input, null);
		assertThat(list.size(), is(expectedJSON.length));
```