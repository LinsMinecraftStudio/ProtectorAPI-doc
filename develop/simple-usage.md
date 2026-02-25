# Simple usage

## Check whether a player can place

Only check a player can place

```java
Player player = ...;

boolean allow = ProtectorAPI.allowPlace(player);
```

If you need to whether a player can place a block at a location (safer than previous method):

```java
Player player = ...;
Block block = ...;

boolean allow = ProtectorAPI.allowPlace(player, block);
```

## Check whether a player can break

Only check a player can break

```java
Player player = ...;

boolean allow = ProtectorAPI.allowBreak(player);
```

If you need to whether a player can break a block at a location (safer than previous method):

```java
Player player = ...;
Block block = ...;

boolean allow = ProtectorAPI.allowBreak(player, block);
```

## Check whether a player can interact

**NOTE: RedProtect didn't have a more general interaction flag, so we uses** [**"redstone"**](#user-content-fn-1)[^1] **flag to check instead. (Although this is not very accurate)**

Only check a player can interact

```java
Player player = ...;

boolean allow = ProtectorAPI.allowInteract(player);
```

If you need to whether a player can interact block at a location (safer than previous method):

```java
Player player = ...;
Block block = ...;

boolean allow = ProtectorAPI.allowInteract(player, block);
```

## Check a event was fired by Protection Plugin is fake

<mark style="color:red;">**Note: v2.0.0 removed this**</mark>

```java
Event event = ...;
boolean fake = ProtectorAPI.isEventFake(event);
```

[^1]: The "redstone" flag in RedProtect allows other players to interact with redstone systems. _Levers and buttons have their own flags_
