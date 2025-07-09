# Simple usage

### Check whether a player can place

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

### Check whether a player can break

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

### Check whether a player can interact

**NOTE: RedProtect didn't have a more general interaction flag, so it uses** [**"redstone"**](#user-content-fn-1)[^1] **flag to check instead.**

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

[^1]: The "redstone" flag in RedProtect allows other players to interact with redstone systems. _Lever and buttons have your own flag_
