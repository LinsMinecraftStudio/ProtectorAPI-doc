# Protection Range Info

## Description

**A ProtectionRangeInfo is the information of the protection range.**

**What can it do?**

1. **get flag state/value**
2. **get admins**
3. **get members**
4. **get the owner**

## Get it by location

```java
Location location = ...;

IProtectionModule module = ProtectorAPI.findModule(location);
if (module == null) {
    return;
}

ProtectionRangeInfo range = module.getProtectionRangeInfo(location);
```

