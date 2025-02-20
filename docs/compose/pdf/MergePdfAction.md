# <small>:nut_and_bolt:</small> Merge

Merges multiple PDF documents into one with a page for each input document.

### Accepts

  - `application/pdf`

### Outputs

  - `application/pdf`

### Usage

```js
{
  "kind": "PdfMerge",
  "chunkLength": null
}
```
#### Properties

**`chunkLength`**  `int32?`

If specified, then documents will be grouped into chunks no larger than this amount. 
Each chunk will then be merged into a PDF document with a page for each document in the chunk.

**Note** the last document might contain less pages than this number if there are not enough input
documents to fill the last chunk.


