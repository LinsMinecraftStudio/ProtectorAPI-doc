# Create your own module

## Protection Module

### Steps

1. Implement `io.github.lijinhong11.protector.api.protection   .IProtectionModule`&#x20;
2. Then create a class to connect your own protection range with the protection range defined by ProtectorAPI, the class must implement `io.github.lijinhong11.protector.api.protection   .IProtectionRange`&#x20;
3. If your module can be used for registering flags, the class must implement `io.github.lijinhong11.protector.api.flag.FlagRegisterable`  **(Since v1.0.9)**

### Register

```java
ProtectorAPI.register(module);
```

## Block Protection Module

### Steps

1. Implement `io.github.lijinhong11.protector.api.block   .IBlockProtectionModule`&#x20;

### Register

```java
ProtectorAPI.register(module);
```
