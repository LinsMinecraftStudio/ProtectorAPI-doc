# Block Protection Modules

## Description

A block protection module can only check the blocks' protection.

What can it do:

1. Check a player can break/place/interact the block

## Check a player can break/place/interact the block

```java
Location location = ...;
Player player = ...;

IBlockProtectionModule module = ProtectorAPI.findBlockModule(location);
if (module == null) {
    return;
}

//check it is being protected
if (!module.isProtected(player, location)) {
    return;
}

//break
boolean b = module.allowBreak(player, location);

//place
boolean b = module.allowPlace(player, location);

//interact
boolean b = module.allowInteract(player, location);
```
