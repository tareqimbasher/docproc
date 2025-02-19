# GetText

Extracts text from PDF documents.

### Supported Inputs

  - `application/pdf`

### Possible Outputs

  - `text/plain`

### JSON

```js
{
  "kind": "PdfGetText",
  "followLayout": false
}
```
### Properties

  - `followLayout` [`Boolean`]: Attempt to follow the layout of the document when extracting text.
