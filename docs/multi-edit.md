# Multi Edit

Express document transformations in a single request using a collection of [`Actions`](#introduction).

## Actions

Actions are a way to express a transformation of a document. Chaining multiple actions can be a powerful way to create
edit workflows quickly and efficiently.

Actions are executed sequentially. When an action runs, it receives the "**active document**" being processed as input,
and outputs a transformed document for the next action to operate on, which then becomes the new "**active document**".

Actions can make edits to the same document, or can entirely convert a document from one type to another. In the example
below, the request will mail merge a Word document, then convert it to a PDF document, then finally compresses it and
return. Calling the API with this payload will give you back in a compressed PDF version of the mail merged document.

```js
[
  {
    "kind": "WordMailMerge",
    "data": {
      "FirstName": "John",
      "LastName": "Doe"
    }
  },
  {
    "kind": "WordConvertToPdf"
  },
  {
    "kind": "PdfCompress"
  }
]
```

## Common Options

All actions have the following options that will not be repeated for brevity:

```js
{
  "kind": "--ActionKind--",
  "continueOnError": false
}
```

- `kind`: **Required** Specifies the type of the action.
- `continueOnError`: Whether to move on to the next step if an error occurs. _default:_ `false`
