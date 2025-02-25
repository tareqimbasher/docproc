# <small>:nut_and_bolt:</small> ReplaceText

Find and replace text in Word documents.
   
### Formats

This action can accept and produce the following content type formats.

| Accepts | Produces |
|-----|-----|
|<ul><li>`application/vnd.openxmlformats-officedocument.wordprocessingml.document` _(.docx)_</li><li>`application/vnd.openxmlformats-officedocument.wordprocessingml.template` _(.dotx)_</li></ul>|<ul><li>`application/vnd.openxmlformats-officedocument.wordprocessingml.document` _(.docx)_</li><li>`application/vnd.openxmlformats-officedocument.wordprocessingml.template` _(.dotx)_</li></ul>|

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
### Properties

**`findText`**  `string` **Required**

The text to replace.


**`replaceText`**  `string` **Required**

The text to use as replacement.


**`caseSensitive`**  `boolean?`

Perform a case-sensitive search.


**`wholeWord`**  `boolean`

Match only whole words.


