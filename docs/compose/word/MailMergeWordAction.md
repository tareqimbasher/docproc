# <small>:nut_and_bolt:</small> MailMerge

Executes a Word mail merge.
   
### Formats

This action can accept and produce the following content type formats.

| Accepts | Produces |
|-----|-----|
|<ul><li>`application/vnd.openxmlformats-officedocument.wordprocessingml.document` _(.docx)_</li><li>`application/vnd.openxmlformats-officedocument.wordprocessingml.template` _(.dotx)_</li></ul>|<ul><li>`application/vnd.openxmlformats-officedocument.wordprocessingml.document` _(.docx)_</li><li>`application/vnd.openxmlformats-officedocument.wordprocessingml.template` _(.dotx)_</li></ul>|

### Usage

```js
{
  "kind": "WordMailMerge",
  "data": {},
  "clearEmptyFields": true,
  "unspecifiedFieldValue": null
}
```
### Properties

**`data`**  `idictionary<string, string>` **Required**

A hashmap of merge field data used to populate mail merge fields in a Word document.
The keys represent the names of the merge fields, and the values contain the text that will replace
each corresponding field during the merge process.


**`clearEmptyFields`**  `boolean`

Whether to remove empty mail merge fields. Default is **true**.


**`unspecifiedFieldValue`**  `string`

The value to set any merge field that is not specified in the data mapping. If this property is left null or unspecified, those fields will remain unchanged.


