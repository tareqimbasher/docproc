# <small>:nut_and_bolt:</small> Pluck

Selects the specified documents and discards the rest.

### Accepts

  - `Any`

### Outputs

  - `Any`

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


