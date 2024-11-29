# Sequence Generation Utilities
<p>Provides helper methods to create sequence numbers. This module can be used on server side only.</p>

## getSequence 
<p>
  Returns nex number for given context and keys for the domain that process has been started. 
</p>
<p>
  Checks last generated number for given keys and returns next number (1 if not found). 
  This number will be saved to DB and next call will increase it again. 
  If context is not specified, it will be used from Config.CONTEXT variable, or $CONTEXT variable of pool.
</p>

> [!IMPORTANT]
> This mehod uses a lock for given key, and lock will be released after process execution is committed. Until then, all processes trying to generate sequence over same key will be blocked.

Syntax:

```js
int getSequence([context,] key1, key2...)
```

Examples:

```js
var year = (new Date()).getFullYear();
var departmentCode = 40;
var sequence = AltiKareUtils.Sequence.getSequence(year, departmentCode, "REF_NUM");
var refNum = "ABC-" + year + "-" + departmentCode + "-" + AltiKareUtils.Text.padLeft(sequence, 6);
console.log(refNum);
// ABC-2024-40-0000012
```

## getGlobalSequence
<p>
  Returns nex number for given context and keys globally. 
</p>
<p>
  This method is same as getSequence, except it will use Global DB to generate numbers.
</p>
Syntax:

```js
int getGlobalSequence([context,] key1, key2...)
```
