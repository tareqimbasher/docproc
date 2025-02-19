# ReplaceText

Find and replace text in Word documents.

### Supported Inputs

  - `application/vnd.openxmlformats-officedocument.wordprocessingml.document`
  - `application/vnd.openxmlformats-officedocument.wordprocessingml.template`

### Possible Outputs

  - `application/vnd.openxmlformats-officedocument.wordprocessingml.document`

### JSON

```js
{
  "kind": "WordReplaceText",
  "findText": null,
  "replaceWithText": null,
  "caseSensitive": true,
  "wholeWord": false
}
```
### Properties

  - `findText` [`String`] **Required**: The text to replace.
  - `replaceWithText` [`String`] **Required**: The text to replace with.
  - `caseSensitive` [`Boolean?`]: Perform a case-sensitive search.
  - `wholeWord` [`Boolean`]: Match only whole word.
