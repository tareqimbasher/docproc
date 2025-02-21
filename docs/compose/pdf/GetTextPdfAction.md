# <small>:nut_and_bolt:</small> GetText

Extracts text from PDF documents.

### Accepts

  - `application/pdf` _(.pdf)_

### Produces

  - `text/plain` _(.txt)_

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


