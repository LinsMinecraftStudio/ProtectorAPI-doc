# Block Protection Modules

## Description

A block protection module can only check the blocks' protection.

It can check whether a player can break/place/interact the block

## Check a player can break/place/interact the block

Example:

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

## Register flags

Since v1.0.9, some block protection modules can register flags.

Example:

```java
IBlockProtectionModule module = ...;
CustomFlag flag = ...;

if (module instanceof FlagRegisterable fr) {
    fr.registerFlag(flag);
}
```

