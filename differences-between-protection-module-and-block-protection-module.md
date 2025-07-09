# Differences between Protection Module & Block Protection Module

## Protection Module

A protection module corresponds to a fully functional plugin that can serve as the primary protection plugin in the server.

### Get by block location

<pre class="language-java"><code class="lang-java"><strong>IProtectionModule module = ProtectorAPI.findModule(location);
</strong></code></pre>

## Block Protection Module

The plugin corresponding to a block protection module is generally a plugin that only has protective properties for blocks (however, Lands is an exception)

### Get by block location and player

```java
IBlockProtectionModule module = ProtectorAPI.findBlockModule(player, location);
```
