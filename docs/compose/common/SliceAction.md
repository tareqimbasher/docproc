# <small>:nut_and_bolt:</small> Slice

Selects a range of documents and discards the rest.
   
### Formats

This action accepts and produces the following content type formats.

| Accepts | Produces |
|-----|-----|
|<ul><li>`text/plain` _(.txt)_</li><li>`application/vnd.openxmlformats-officedocument.wordprocessingml.document` _(.docx)_</li><li>`application/vnd.openxmlformats-officedocument.wordprocessingml.template` _(.dotx)_</li><li>`application/pdf` _(.pdf)_</li><li>`image/png` _(.png)_</li><li>`image/jpeg` _(.jpg)_</li><li>`image/webp` _(.webp)_</li><li>`image/bmp` _(.bmp)_</li><li>`image/heif` _(.heif)_</li><li>`application/zip` _(.zip)_</li></ul>|<ul><li>`text/plain` _(.txt)_</li><li>`application/vnd.openxmlformats-officedocument.wordprocessingml.document` _(.docx)_</li><li>`application/vnd.openxmlformats-officedocument.wordprocessingml.template` _(.dotx)_</li><li>`application/pdf` _(.pdf)_</li><li>`image/png` _(.png)_</li><li>`image/jpeg` _(.jpg)_</li><li>`image/webp` _(.webp)_</li><li>`image/bmp` _(.bmp)_</li><li>`image/heif` _(.heif)_</li><li>`application/zip` _(.zip)_</li></ul>|

### Usage

```js
{
  "kind": "Slice",
  "skip": null,
  "take": null,
  "reverse": false
}
```
### Properties

**`skip`**  `int32?`

How many items to skip.


**`take`**  `int32?`

How many items to take.


**`reverse`**  `boolean`

Whether to skip/take starting from the end; ie. `Skip = 1` in this case will skip the last document.


