# <small>:nut_and_bolt:</small> Slice

Selects a range of documents and discards the rest.

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

### Usage

```js
{
  "kind": "Slice",
  "skip": null,
  "take": null,
  "reverse": false
}
```
#### Properties

**`skip`**  `int32?`

How many items to skip.


**`take`**  `int32?`

How many items to take.


**`reverse`**  `boolean`

Whether to skip/take starting from the end; ie. `Skip = 1` in this case will skip the last document.


