# Configuration Utilities
<p>Provides helper methods to retrieve and store configurative values. This module can be used on server side only.</p>

## hasGlobalDB 
<p>
  Returns true if current domain has parent multi-tenant configuration DB.
</p>
<p>
  This method is mainly used by internal methods, and configuration user interfaces.
</p>

```
AltiKare.Workflow.Agent.exe registerstore "mycompany.com" "PS_GLB" "AltiKareUtils.txt"
```

Syntax:

```js
bool hasGlobalDB()
```

Examples:

```js
console.log(AltiKareUtils.Config.hasGlobalDB());
// false
```

## escape
<p>Escapes value to be used directly in XML as string.</p>

## unescape
<p>Unescapes value escaped for XML.</p>

## padLeft
<p>Converts a value to padded string.</p>

## setValueAndCaption
<p>Profides a helper to set both value and "Caption" attribute of path.</p>

## toObject
<p>Converts given XML to javascript object.</p>

## toJSON
<p>Converts given XML to object, then JSON string.</p>

## toArray
<p>Converts given XML to javascript array.</p>
