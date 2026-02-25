---
metaLinks:
  alternates:
    - https://app.gitbook.com/s/vLjgle6jl104vuDDoA0T/develop/simple-usage
---

# 简单用法

## 检查玩家是否可以放置方块

只检查玩家是否可以放置方块（不论最终放置的方块在哪）

```java
Player player = ...;

boolean allow = ProtectorAPI.allowPlace(player);
```

如果你要检查玩家是否可以放置方块在某个位置（比上个方法更安全）：

```java
Player player = ...;
Block block = ...;

boolean allow = ProtectorAPI.allowPlace(player, block);
```

## 检查玩家是否可以破坏方块

只检查玩家是否可以破坏方块（不论最终放置的方块在哪）

```java
Player player = ...;

boolean allow = ProtectorAPI.allowBreak(player);
```

如果你要检查玩家是否可以破坏某个位置的方块（比上个方法更安全）：

```java
Player player = ...;
Block block = ...;

boolean allow = ProtectorAPI.allowBreak(player, block);
```

## 检查玩家是否可以交互

**注意: RedProtect 没有通用的交互标志，所以使用**  [**"redstone"**](#user-content-fn-1)[^1] **标志进行检查。**

只检查玩家是否可以交互方块（不论最终放置的方块在哪）

```java
Player player = ...;

boolean allow = ProtectorAPI.allowInteract(player);
```

如果你要检查玩家是否可以与某个位置的方块进行交互（比上个方法更安全）：

```java
Player player = ...;
Block block = ...;

boolean allow = ProtectorAPI.allowInteract(player, block);
```

## 检查由保护插件发出的事件是否为假事件

<mark style="color:red;">**注意：v2.0.0已移除**</mark>

```java
Event event = ...;
boolean fake = ProtectorAPI.isEventFake(event);
```

[^1]: RedProtect中的redstone标志是允许/禁止玩家与红石系统交互。_按钮和拉杆都有他们自己的标志。_
