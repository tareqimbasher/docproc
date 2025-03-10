# <small>:nut_and_bolt:</small> Compress

Compresses PDF documents.
   
### Formats

This action can accept and produce the following content type formats.

| Accepts | Produces |
|-----|-----|
|<ul><li>`application/pdf` _(.pdf)_</li></ul>|<ul><li>`application/pdf` _(.pdf)_</li></ul>|

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
### Properties

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


