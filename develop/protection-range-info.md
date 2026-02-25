---
metaLinks:
  alternates:
    - >-
      https://app.gitbook.com/s/vLjgle6jl104vuDDoA0T/develop/protection-range-info
---

# 保护范围信息

## 描述

**一个保护范围信息就是该保护范围的信息**

**它能做什么？**

1. **获取标志的值**
2. **获取管理**
3. **获取成员**
4. **获取所有者**

## 通过位置获取

```java
Location location = ...;

IProtectionModule module = ProtectorAPI.findModule(location);
if (module == null) {
    return;
}

IProtectionRangeInfo range = module.getProtectionRangeInfo(location);
```

