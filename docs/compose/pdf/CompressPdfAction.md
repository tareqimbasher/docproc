# <small>:nut_and_bolt:</small> Compress

Compresses PDF documents.

### Accepts

  - `application/pdf`

### Outputs

  - `application/pdf`

### Usage

```js
{
  "kind": "PdfCompress",
  "compressImages": true,
  "imageQuality": 50,
  "optimizeFont": true,
  "optimizePageContents": true,
  "removeMetadata": false
}
```
#### Properties

**`compressImages`**  `boolean`

Whether or not to compress images.


**`imageQuality`**  `int32`

A value between 1 and 100.


**`optimizeFont`**  `boolean`

Whether or not to optimize fonts.


**`optimizePageContents`**  `boolean`

Whether or not to optimize page contents.


**`removeMetadata`**  `boolean`

Whether or not to remove metadata from documents.


