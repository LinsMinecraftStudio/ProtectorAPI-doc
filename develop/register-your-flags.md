---
metaLinks:
  alternates:
    - https://app.gitbook.com/s/vLjgle6jl104vuDDoA0T/develop/register-your-flags
---

# 注册标志

## 描述

自 v1.0.5, 你可以注册一个标志

## 怎么做

为了注册标志，你需要先创建一个 `CustomFlag` 实例

`CustomFlag` 的类结构:

```java
package io.github.lijinhong11.protector.api.flag;

import org.jetbrains.annotations.NotNull;
import org.jetbrains.annotations.Nullable;

/**
 * The custom flag object
 * @param namespace the namespace for verify
 * @param id the flag ID
 * @param defaultValue the default value
 * @param displayName the display name of the flag (optional)
 * @param description the description about the flag (optional)
 */
public record CustomFlag(@NotNull String namespace, @NotNull String id, boolean defaultValue, @Nullable String displayName, @Nullable String description) {
}
```

创建实例后，你可以按照以下方法注册：

```java
CustomFlag flag = ...;
ProtectorAPI.registerFlag(flag);
```
