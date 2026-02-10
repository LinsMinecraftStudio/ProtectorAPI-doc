---
metaLinks:
  alternates:
    - https://app.gitbook.com/s/vLjgle6jl104vuDDoA0T/develop/protection-modules
---

# 保护模块

## **描述**

**一个保护模块可以做很多事，但是取决于对应的保护插件。**

它能做什么：

1. 通过 玩家/位置 获取一个保护范围
2. 检查 玩家/位置 是否在一个保护范围内
3. 获取玩家名下所有的保护范围 (功能并不完全)
4. 获取/设置 全局标志

## 获取保护模块

这里有4种方式：

第一：

```java
IProtectionModule module = ProtectorAPI.findModule(location);
```

第二 (自 v1.0.2):

```java
IProtectionModule module = ProtectorAPI.getModuleByPluginName(pluginName);
```

第三 (自 v1.0.3, 可能不是你想要的):

```java
IProtectionModule module = ProtectorAPI.getFirstAvailableModule();
```

第四 (自 v1.0.5):

```java
Collection<IProtectionModule> modules = ProtectorAPI.getAllAvailableProtectionModules();
```

## 获取一个保护范围

参阅 [Protection Range Info](protection-range-info.md)&#x20;

## Check a player/location is in any protection range

```java
Location location = ...;
Player p = ...;

IProtectionModule module = ProtectorAPI.findModule(location);
if (module == null) {
    return;
}

boolean b = module.isInProtectionRange(location);

//OR
boolean b = module.isInProtectionRange(p);
```

## Get all protection ranges by a player

```java
OfflinePlayer p = ...;
IProtectionModule module = ...;
List<? extends ProtectionRangeInfo> range = module.getProtectionRangeInfos(p);
```

## Get/Set global flags

**NOTE: Some plugins don't support global flags, so when executing the method, it will throw an `UnsupportedOperationException`.**&#x20;

```java
boolean supported = module.isSupportGlobalFlags();
if (!supported) {
    return;
}

IFlagState<?> value = module.getGlobalFlag("break", "worldName");
boolean allowBreak = (boolean) value.getValue();

module.setGlobalFlag("break", "worldName", true);
```
