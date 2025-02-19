# <small>:nut_and_bolt:</small> Create

Creates a zip file from a group of documents.

### Accepts

  - `Any`

### Outputs

  - `application/zip`

### Usage

```js
{
  "kind": "ZipCreate",
  "level": null
}
```
#### Properties

**`level`**  `compressionlevel?`

If specified, sets the compression level of the zip file. Options:
  
  - Optimal
  - Fastest
  - NoCompression
  - SmallestSize


