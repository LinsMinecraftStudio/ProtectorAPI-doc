# Protection Modules

## **Description**

**A protection module can be used to do many things, depends on the corresponding plugin.**

What can it do:

1. Get a protection range by player/location
2. Check a player/location is in any protection range
3. Get all protection ranges by a player (feature not completed)
4. Get/Set global flags

## Get protection module

There're 2 ways of getting the protection module:

No.1:

```java
IProtectionModule module = ProtectorAPI.findModule(location);
```

No.2:

```java
IProtectionModule module = ProtectorAPI.getModuleByPluginName(pluginName);
```

## Get a protection range

See [Protection Range Info](protection-range-info.md) for details.&#x20;

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

**NOTE: Some plugins don't support global flags, so when executing the method, it will throw an UnsupportedOperationException.**&#x20;

```java
boolean supported = module.isSupportGlobalFlags();
if (!supported) {
    return;
}

IFlagState<?> value = module.getGlobalFlag("break", "worldName");
boolean allowBreak = (boolean) value.getValue();

module.setGlobalFlag("break", "worldName", true);
```
