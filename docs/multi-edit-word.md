# Word Actions

Actions that operate on Word documents (`.docx`).

### Replace Text

**Kind:** `WordReplaceText`

```js
{
  "kind": "WordReplaceText",
  "findText": "abc",
  "replaceWithText": "xyz",
  "caseSensitive": false,
  "wholeWord": false
}
```

#### Options

- `findText`: **Required** The text to find and replace.
- `replaceWithText`: **Required** The text to find and replace. Can be an empty string.
- `caseSensitive`: Perform a case-sensitive search. _default:_ `false`
- `wholeWord`: Only match the whole word. _default:_ `false`

### Mail Merge

**Kind:** `WordMailMerge`

```js
{
  "kind": "WordMailMerge",
  "data": {
    "FirstName": "John",
    "LastName": "Doe"
  }
}
```

#### Options

- `data`: **Required** A field-value map of mail merge data.

### Convert to PDF

**Kind:** `WordConvertToPdf`

```js
{
  "kind": "WordConvertToPdf",
}
```
