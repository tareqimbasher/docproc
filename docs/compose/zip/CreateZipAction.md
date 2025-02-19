# Create

Creates a zip file from a group of documents.

### Supported Inputs

  - `Any`

### Possible Outputs

  - `application/zip`

### JSON

```js
{
  "kind": "ZipCreate",
  "level": null
}
```
### Properties

  - `level` [`CompressionLevel?`]: If specified, sets the compression level of the zip file. Options:
  
    - Optimal
    - Fastest
    - NoCompression
    - SmallestSize
