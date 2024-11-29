# XML Utilities
Provides XML helper methods under AltiKareUtils.Xml namespace. Contains following methods;

## parse 
<p>
  Parses string and resturns xml navigator object.
</p>
<p>
  Use this method to parse xml. This method uses related object types for server/client sides and returns object itself if its already a navigator. Otherwise null will be returned. 
</p>
  
Syntax:

```javascript
XmlNavigator parse(strOrXml)
```

Examples:

```javascript
console.log(AltiKareUtils.Xml.parse("<a>5</a>").Evaluate("/a");
// 5
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
