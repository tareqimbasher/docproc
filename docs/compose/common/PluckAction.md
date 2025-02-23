# <small>:nut_and_bolt:</small> Pluck

Selects the specified documents and discards the rest.
   
### Formats

This action accepts and produces the following content type formats.

| Accepts | Produces |
|-----|-----|
|<ul><li>`text/plain` _(.txt)_</li><li>`application/vnd.openxmlformats-officedocument.wordprocessingml.document` _(.docx)_</li><li>`application/vnd.openxmlformats-officedocument.wordprocessingml.template` _(.dotx)_</li><li>`application/pdf` _(.pdf)_</li><li>`image/png` _(.png)_</li><li>`image/jpeg` _(.jpg)_</li><li>`image/webp` _(.webp)_</li><li>`image/bmp` _(.bmp)_</li><li>`image/heif` _(.heif)_</li><li>`application/zip` _(.zip)_</li></ul>|<ul><li>`text/plain` _(.txt)_</li><li>`application/vnd.openxmlformats-officedocument.wordprocessingml.document` _(.docx)_</li><li>`application/vnd.openxmlformats-officedocument.wordprocessingml.template` _(.dotx)_</li><li>`application/pdf` _(.pdf)_</li><li>`image/png` _(.png)_</li><li>`image/jpeg` _(.jpg)_</li><li>`image/webp` _(.webp)_</li><li>`image/bmp` _(.bmp)_</li><li>`image/heif` _(.heif)_</li><li>`application/zip` _(.zip)_</li></ul>|

### Usage

```js
{
  "kind": "Pluck",
  "indexes": [],
  "ignoreOutOfBounds": false
}
```
### Properties

**`indexes`**  `int32[]` **Required**

Indexes (0-based) of the documents to pluck. Items are plucked in this order so this can be used as a way to reorder documents.


**`ignoreOutOfBounds`**  `boolean`

Ignore specified indexes that are out of bounds.


