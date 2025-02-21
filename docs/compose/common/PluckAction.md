# <small>:nut_and_bolt:</small> Pluck

Selects the specified documents and discards the rest.

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
  "kind": "Pluck",
  "indexes": [],
  "ignoreOutOfBounds": false
}
```
#### Properties

**`indexes`**  `int32[]` **Required**

Indexes (0-based) of the documents to pluck. Items are plucked in this order so this can be used as a way to reorder documents.


**`ignoreOutOfBounds`**  `boolean`

Ignore specified indexes that are out of bounds.


