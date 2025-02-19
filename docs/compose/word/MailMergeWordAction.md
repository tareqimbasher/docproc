# MailMerge

Executes a Word mail merge.

### Supported Inputs

  - `application/vnd.openxmlformats-officedocument.wordprocessingml.document`
  - `application/vnd.openxmlformats-officedocument.wordprocessingml.template`

### Possible Outputs

  - `application/vnd.openxmlformats-officedocument.wordprocessingml.document`

### JSON

```js
{
  "kind": "WordMailMerge",
  "data": null,
  "unspecifiedFieldValue": null
}
```
### Properties

  - `data` [`Dictionary`2`] **Required**: A MergeFieldName -> Value map to fill merge fields.
  - `unspecifiedFieldValue` [`String`]: If specified, any merge field that did not occur in the Data mapping will be assigned this value. Otherwise, those fields remain untouched.
