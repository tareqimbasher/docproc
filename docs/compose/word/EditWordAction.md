# <small>:nut_and_bolt:</small> Edit

Applies a series of edits to Word documents. See [Get Structure](/word/get-structure) for a Word document's structure.
   
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

**`edits`**  [`IWordEdit[]`](#IWordEdit) **Required**

The edits to apply to the documents.


### Relevant Types

#### AddEdit :id=IWordEdit

Adds a new node to a Word document.

```js
{
  "op": "Add",
  "path": null,
  "index": null,
  "item": null
}
```

##### Properties

**`path`**  [`NodePath`](#NodePath) **Required**

The path to the containing node where the new item will be inserted. The path target must be a composite node; a node that can hold child nodes.


**`index`**  `int32?`

If specified, the item will be inserted at this index.


**`item`**  [`ICanBeAdded`](#ICanBeAdded) **Required**

The new item to add.


---
#### UpdateEdit :id=IWordEdit

Updates an existing Word document node.

```js
{
  "op": "Update",
  "path": null
}
```

##### Properties

**`path`**  [`NodePath`](#NodePath) **Required**

The path of the node to update.


---
#### RemoveEdit :id=IWordEdit

Removes an existing Word document node.

```js
{
  "op": "Remove",
  "path": null
}
```

##### Properties

**`path`**  [`NodePath`](#NodePath) **Required**

The path of the node to remove.


---
#### CopyEdit :id=IWordEdit

Copies a Word document node to another location.

```js
{
  "op": "Copy",
  "path": null,
  "destPath": null
}
```

##### Properties

**`path`**  [`NodePath`](#NodePath) **Required**

The path of the node to copy.


**`destination`**  [`NodePath`](#NodePath) **Required**

The path of the node to copy to. The target of this path must be a composite node; a node that can hold child nodes.


---
