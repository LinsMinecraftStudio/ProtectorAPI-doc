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

参阅 [Protection Range Info](protection-range.md)&#x20;

## 检查 玩家/位置 是否在一个保护范围内

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

## 获取玩家名下所有的保护范围&#x20;

```java
OfflinePlayer p = ...;
IProtectionModule module = ...;
List<? extends ProtectionRangeInfo> range = module.getProtectionRangeInfos(p);
```

## 获取/设置 全局标志

**注意: 有些插件不支持获取/设置全局标志，所以执行时会抛出 `UnsupportedOperationException` 。**

```java
boolean supported = module.isSupportGlobalFlags();
if (!supported) {
    return;
}

FlagState<?> value = module.getGlobalFlag("break", "worldName");
boolean allowBreak = (boolean) value.getValue();

module.setGlobalFlag("break", "worldName", true);
```
