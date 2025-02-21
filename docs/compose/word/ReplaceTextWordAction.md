# <small>:nut_and_bolt:</small> ReplaceText

Find and replace text in Word documents.

### Accepts

  - `application/vnd.openxmlformats-officedocument.wordprocessingml.document` _(.docx)_
  - `application/vnd.openxmlformats-officedocument.wordprocessingml.template` _(.dotx)_

### Produces

  - `application/vnd.openxmlformats-officedocument.wordprocessingml.document` _(.docx)_

### Usage

```js
{
  "kind": "WordReplaceText",
  "findText": null,
  "replaceText": null,
  "caseSensitive": true,
  "wholeWord": false
}
```
#### Properties

**`findText`**  `string` **Required**

The text to replace.


**`replaceText`**  `string` **Required**

The text to use as replacement.


**`caseSensitive`**  `boolean?`

Perform a case-sensitive search.


**`wholeWord`**  `boolean`

Match only whole words.


