# breakFabricLoom
Just a demo how to break Fabric loom's mixin remapper

In this, I have two modules:  
 - MC 1.16
 - MC 1.18

Both with the *same* mixin. What the mixin does is not important.  

### The bug

In BipedEntityModel [yarn] leftArm has changed the intermediary name: In 1.16.5 it is `field_3390`, but from 1.17 it is `field_27433`.  
The mixin uses this field, so it must be remapped...  

For some reason, the remapping fails to do it correctly, it remap every mixin with the **same** mappings.  
On my computer loom used 1.16.5 mappings for both jars, causing the 1.18 to crash when I try to load it.  


