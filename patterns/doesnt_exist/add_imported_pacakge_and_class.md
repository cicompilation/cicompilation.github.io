---
layout: page
---
## RS485/LogisticsPipes 1137.1

### Error Message

---------------------

```java
/home/travis/build/RS485/LogisticsPipes/dummy/cofh/thermaldynamics/render/RenderDuct.java:3: error: package cofh.repack.codechicken.lib.render does not exist
import cofh.repack.codechicken.lib.render.CCModel;
                                         ^
```

### Code Change

---------------------

***dummy/cofh/repack/codechicken/lib/render/CCModel.java***

```diff
+ package cofh.repack.codechicken.lib.render;
+ import cofh.repack.codechicken.lib.render.CCRenderState.IVertexOperation;
+ public class CCModel {
+ 	public void render(IVertexOperation[] iVertexOperations) {
+		// TODO Auto-generated method stub
		
+	 }
	
+ }
```