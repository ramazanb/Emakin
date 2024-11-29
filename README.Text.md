# Text Utilities
Provides text helper methods under AltiKareUtils.Text namespace. Contains following methods;

## toSearchText 
<p>
  Merges all parameters and returns a single spaced words / numbers all converted to English lower case characters.
</p>
<p>
  Use this method to generate keywords string to be stored on DB (e.g. SearchText or Keywords named field on table). 
  On your reports / search screens, use toSearchTextCriteriaBlock methods to search records with keywords.
</p>
  
<h3>Syntax</h3>

```javascript
string toSearchText(arg1, arg2...)
```

<h3>Examples</h3>

```javascript
console.log(AltiKareUtils.Text.toSearchText("ALİ  doğan ", ".", "1234-5678", null, undefined);
// ali dogan 1234 5678
```

```javascript
var person = AltiKareUtils.Xml.toObject($Xml.SelectSingle("Person"));
person.SearchText = AltiKareUtils.Text.toSearchText(person.Name, person.Surname, person.RegistryNumber);
$Database.EnsureData("HR", "Persons", "Id", person.Id, person);
```

## toSearchTextCriteriaBlock
<p>Creates a keyword criteria block for given arguments.</p>

## toSearchTextCriteria
<p>Creates a keyword criteria array for given arguments.</p>

## padLeft
<p>Converts a value to padded string.</p>

## clearWhitespace
<p>Trims and strips double spaces and other whitespace from string.</p>

## clearHTML
<p>Strips HTML tags off and clears white space from string.</p>

## toTitleCaseTR
<p>Converts given string to "Title Case", handling special Turkish characters.</p>

## toUpperCaseTR
<p>Converts given string to "UPPER CASE", handling special Turkish characters.</p>

## toLowerCaseTR
<p>Converts given string to "lower case", handling special Turkish characters.</p>

## isValidEmail
<p>Checks whether given string is a valid email address.</p>

## toObject
<o>Converts parameter (JSON string or other) into object.</p>

## toJSON
<p>Converts parameter (string or object) into JSON string.</p>
