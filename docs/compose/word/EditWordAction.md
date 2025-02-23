# <small>:nut_and_bolt:</small> Edit

Applies a series of edits to Word documents.
   
### Formats

This action accepts and produces the following content type formats.

| Accepts | Produces |
|-----|-----|
|<ul><li>`application/vnd.openxmlformats-officedocument.wordprocessingml.document` _(.docx)_</li><li>`application/vnd.openxmlformats-officedocument.wordprocessingml.template` _(.dotx)_</li></ul>|<ul><li>`application/vnd.openxmlformats-officedocument.wordprocessingml.document` _(.docx)_</li><li>`application/vnd.openxmlformats-officedocument.wordprocessingml.template` _(.dotx)_</li></ul>|

### Usage

```js
{
  "kind": "WordEdit",
  "edits": []
}
```
#### Properties

**`edits`**  `iwordedit[]` **Required**

The edits to make to the documents.


