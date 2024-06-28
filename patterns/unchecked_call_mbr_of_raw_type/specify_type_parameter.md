---
layout: page
---
## TVPT/VoxelSniper 34.1

### Warning Message

---------------------

```java
/home/travis/build/TVPT/VoxelSniper/build/sources/java/com/voxelplugineering/voxelsniper/sponge/util/SpongeUtilities.java:61: warning: [unchecked] unchecked call to Location(E,Vector3d) as a member of the raw type Location
return new org.spongepowered.api.world.Location(((SpongeWorld) location.getWorld()).getThis(), getSpongeVector(location.toVector()));
^
where E is a type-variable:
E extends Extent declared in class Location
```

### Code Change

---------------------

***.travis.yml***

```diff
-        return new org.spongepowered.api.world.Location(((SpongeWorld) location.getWorld()).getThis(), getSpongeVector(location.toVector()));
+        return new org.spongepowered.api.world.Location<org.spongepowered.api.world.World>(((SpongeWorld) location.getWorld()).getThis(),
+                getSpongeVector(location.toVector()));
```