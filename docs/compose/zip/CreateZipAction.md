# <small>:nut_and_bolt:</small> Create

Creates a zip file from a group of documents.

### Accepts

  - `text/plain` _(.txt)_
  - `application/vnd.openxmlformats-officedocument.wordprocessingml.document` _(.docx)_
  - `application/vnd.openxmlformats-officedocument.wordprocessingml.template` _(.dotx)_
  - `application/pdf` _(.pdf)_
  - `image/png` _(.png)_
  - `image/jpeg` _(.jpg)_
  - `image/webp` _(.webp)_
  - `image/bmp` _(.bmp)_
  - `image/heif` _(.heif)_
  - `application/zip` _(.zip)_

### Produces

  - `application/zip` _(.zip)_

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


