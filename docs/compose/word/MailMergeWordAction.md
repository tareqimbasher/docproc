# <small>:nut_and_bolt:</small> MailMerge

Executes a Word mail merge.

### Accepts

  - `application/vnd.openxmlformats-officedocument.wordprocessingml.document` _(.docx)_
  - `application/vnd.openxmlformats-officedocument.wordprocessingml.template` _(.dotx)_

### Produces

  - `application/vnd.openxmlformats-officedocument.wordprocessingml.document` _(.docx)_

### Usage

```js
{
  "kind": "WordMailMerge",
  "data": {},
  "unspecifiedFieldValue": null
}
```
#### Properties

**`data`**  `dictionary<string, string>` **Required**

A hashmap of merge field data used to populate mail merge fields in a Word document.
The keys represent the names of the merge fields, and the values contain the text that will replace
each corresponding field during the merge process.


**`unspecifiedFieldValue`**  `string`

Gets or sets the text to apply to any merge fields that are not found in the data mapping.If this property is left null or unspecified, those fields will remain unchanged.


