# Configuration Utilities
<p>Provides helper methods to retrieve and store configurative values. This module can be used on server side only.</p>

## hasGlobalDB 
<p>
  Returns true if current domain has parent multi-tenant configuration DB.
</p>
<p>
  This method is mainly used by internal methods, and configuration user interfaces.
</p>

Syntax:

```js
bool hasGlobalDB([reset])
```

Examples:

```js
console.log(AltiKareUtils.Config.hasGlobalDB());
// false
```

## resolveContext
<p>Returns process defined context if given parameter is empty.</p>
<p>This method is mainly used by internal methods, and configuration user interfaces.</p>

Syntax:

```js
string resolveContext([context])
```

## getConfig
<p>Reads configuration for domain, then global if no config found and global DB configured.</p>

## getDomainConfig
<p>Reads configuration for domain.</p>

## getGlobalConfig
<p>Converts given XML to object, then JSON string.</p>
<p>DB error might occour and your process might be stopped if global (multi-tenant) DB is not configured.</p>

## getIdentityConfig
<p>Reads configuration for given identity.</p>

## invalidateCache
<p>Removes all keys from cache.</p>

## parseConfigValue
<p>Parses given value by config. type.</p>
<p>This method is mainly used by internal methods, and configuration user interfaces.</p>

## setDomainConfig
<p>Sets configuration for domain.</p>

## setIdentityConfig
<p>Sets configuration for identity</p>

## setGlobalConfig
<p>Sets global  (multi-tenant) configuration.</p>
