# <small>:nut_and_bolt:</small> ReplaceText

Find and replace text in Word documents.

### Accepts

  - `application/vnd.openxmlformats-officedocument.wordprocessingml.document`
  - `application/vnd.openxmlformats-officedocument.wordprocessingml.template`

### Outputs

  - `application/vnd.openxmlformats-officedocument.wordprocessingml.document`

### Usage

```js
{
  "kind": "WordReplaceText",
  "findText": null,
  "replaceWithText": null,
  "caseSensitive": true,
  "wholeWord": false
}
```
#### Properties

**`findText`**  `string` **Required**

The text to replace.


**`replaceWithText`**  `string` **Required**

The text to replace with.


**`caseSensitive`**  `boolean?`

Perform a case-sensitive search.


**`wholeWord`**  `boolean`

Match only whole word.


