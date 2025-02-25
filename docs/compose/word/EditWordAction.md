# <small>:nut_and_bolt:</small> Edit

Applies a series of edits to Word documents.
   
### Formats

This action can accept and produce the following content type formats.

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
### Properties

**`edits`**  `IWordEdit[]` **Required**

The edits to apply to the documents.


### Types

##### `IWordEdit`

Implementations:

**`AddEdit`**

```js
{
  "op": "Add",
  "path": null,
  "index": null,
  "item": null
}
```

**`UpdateEdit`**

```js
{
  "op": "Update",
  "path": null
}
```

**`RemoveEdit`**

```js
{
  "op": "Remove",
  "path": null
}
```

**`CopyEdit`**

```js
{
  "op": "Copy",
  "path": null,
  "destPath": null
}
```

