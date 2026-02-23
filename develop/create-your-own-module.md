---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/vLjgle6jl104vuDDoA0T/develop/create-your-own-module
---

# 创建属于你自己的模块

## 保护模块

### 步骤

第一步，实现 `io.github.lijinhong11.protector.api.protection.IProtectionModule`&#x20;

然后创建一个类，将您自己的保护范围与ProtectorAPI定义的保护范围连接起来，该类必须实现 `io.github.lijinhong11.protector.api.protection.ProtectionRangeInfo`&#x20;

如果你的保护模块可以被用来注册标志，保护模块类必须实现`io.github.lijinhong11.protector.api.flag.FlagRegisterable`  **(自 v1.0.9)**

### 注册

```java
ProtectorAPI.register(module);
```

## Block Protection Module

### 步骤

实现 `io.github.lijinhong11.protector.api.block.IBlockProtectionModule`&#x20;

### 注册

```java
ProtectorAPI.register(module);
```
