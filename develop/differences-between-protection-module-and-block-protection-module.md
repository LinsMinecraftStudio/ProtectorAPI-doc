---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/vLjgle6jl104vuDDoA0T/develop/differences-between-protection-module-and-block-protection-module
---

# 保护模块与方块保护模块之间的不同

## 保护模块

保护模块对应于一个功能完整的插件，可在服务器中充当主要保护插件

### 通过方块位置获取

```java
IProtectionModule module = ProtectorAPI.findModule(location);
```

## 方块保护模块

方块保护模块对应的插件通常仅具备方块保护功能（但Lands、ExcellentClaims和HuskClaims是例外）

### 通过方块位置和玩家获取

```java
IBlockProtectionModule module = ProtectorAPI.findBlockModule(player, location);
```
