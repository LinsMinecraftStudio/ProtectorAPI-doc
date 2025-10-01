# Create your own module

## Protection Module

### Steps

First, implement `io.github.lijinhong11.protector.api.protection.IProtectionModule`&#x20;

Then create a class to connect your own protection range with the protection range defined by ProtectorAPI, the class must implement `io.github.lijinhong11.protector.api.protection.ProtectionRangeInfo`&#x20;

If your module can be used for registering flags, the class must implement `io.github.lijinhong11.protector.api.flag.FlagRegisterable`  **(Since v1.0.9)**

### Register

just use the method below:

```java
ProtectorAPI.register(module);
```

## Block Protection Module

### Steps

Implement `io.github.lijinhong11.protector.api.block.IBlockProtectionModule`&#x20;

### Register

just use the method below:

```java
ProtectorAPI.register(module);
```
