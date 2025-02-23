# <small>:nut_and_bolt:</small> GetText

Extracts text from PDF documents.
   
### Formats

This action accepts and produces the following content type formats.

| Accepts | Produces |
|-----|-----|
|<ul><li>`application/pdf` _(.pdf)_</li></ul>|<ul><li>`text/plain` _(.txt)_</li></ul>|

### Usage

```js
{
  "kind": "PdfGetText",
  "followLayout": false
}
```
#### Properties

**`followLayout`**  `boolean`

Attempt to follow the layout of the document when extracting text.


