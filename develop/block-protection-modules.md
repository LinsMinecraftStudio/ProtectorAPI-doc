---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/vLjgle6jl104vuDDoA0T/develop/block-protection-modules
---

# 方块保护模块

## 描述

一个方块保护模块仅可以检查对一个方块的保护情况

它可以检查玩家是否可以  破坏/放置/交互 该位置的方块

## 检查玩家是否可以 破坏/放置/交互 该位置的方块

示例:

```java
Location location = ...;
Player player = ...;

IBlockProtectionModule module = ProtectorAPI.findBlockModule(location);
if (module == null) {
    return;
}

if (!module.isProtected(player, location)) {
    return;
}

boolean break = module.allowBreak(player, location);

boolean place = module.allowPlace(player, location);

boolean interact = module.allowInteract(player, location);
```

## 注册标志

自 v1.0.9，有些方块保护模块可以注册标志

示例:

```java
IBlockProtectionModule module = ...;
CustomFlag flag = ...;

if (module instanceof FlagRegisterable fr) {
    fr.registerFlag(flag);
}
```

