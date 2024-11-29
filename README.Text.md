# Text Utilities
Provides text helper methods under AltiKareUtils.Text namespace. Contains following methods;

## toSearchText 
<details>
  <summary>Merges all parameters and returns a single spaced words / numbers all converted to English lower case characters.</summary>
<p>
  Use this method to generate keywords string to be stored on DB (e.g. SearchText or Keywords named field on table). 
  On your reports / search screens, use toSearchTextCriteriaBlock methods to search records with keywords.
</p>
  
### Syntax:

```javascript
string toSearchText(arg1, arg2...)
```

### Examples:

```javascript
console.log(AltiKareUtils.Text.toSearchText("ALİ  doğan ", ".", "1234-5678", null, undefined);
// ali dogan 1234 5678
```

```javascript
var person = AltiKareUtils.Xml.toObject($Xml.SelectSingle("Person"));
person.SearchText = AltiKareUtils.Text.toSearchText(person.Name, person.Surname, person.RegistryNumber);
$Database.EnsureData("HR", "Persons", "Id", person.Id, person);
```
</details>

## toSearchTextCriteriaBlock
<details>
  <summary>Creates a keyword criteria block for given arguments.</summary>
</details>

## toSearchTextCriteria
<details>
  <summary>Creates a keyword criteria array for given arguments.</summary>
</details>

## padLeft
<details>
  <summary>Converts a value to padded string.</summary>
</details>

## clearWhitespace
<details>
  <summary>Trims and strips double spaces and other whitespace from string.</summary>
</details>

## clearHTML
<details>
  <summary>Strips HTML tags off and clears white space from string.</summary>
</details>

## toTitleCaseTR
<details>
  <summary>Converts given string to "Title Case", handling special Turkish characters.</summary>
</details>

## toUpperCaseTR
<details>
  <summary>Converts given string to "UPPER CASE", handling special Turkish characters.</summary>
</details>

## toLowerCaseTR
<details>
  <summary>Converts given string to "lower case", handling special Turkish characters.</summary>
</details>

## isValidEmail
<details>
  <summary>Checks whether given string is a valid email address.</summary>
</details>

## toObject
<details>
  <summary>Converts parameter (JSON string or other) into object.</summary>
</details>

## toJSON
<details>
  <summary>Converts parameter (string or object) into JSON string.</summary>
</details>
