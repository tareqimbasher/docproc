# <small>:nut_and_bolt:</small> Create

Creates a zip file from a group of documents.
   
### Formats

This action accepts and produces the following content type formats.

| Accepts | Produces |
|-----|-----|
|<ul><li>`text/plain` _(.txt)_</li><li>`application/vnd.openxmlformats-officedocument.wordprocessingml.document` _(.docx)_</li><li>`application/vnd.openxmlformats-officedocument.wordprocessingml.template` _(.dotx)_</li><li>`application/pdf` _(.pdf)_</li><li>`image/png` _(.png)_</li><li>`image/jpeg` _(.jpg)_</li><li>`image/webp` _(.webp)_</li><li>`image/bmp` _(.bmp)_</li><li>`image/heif` _(.heif)_</li><li>`application/zip` _(.zip)_</li></ul>|<ul><li>`application/zip` _(.zip)_</li></ul>|

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


