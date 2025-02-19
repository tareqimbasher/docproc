# <small>:nut_and_bolt:</small> Pluck

Selects any number of documents and discards the rest.

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

0-based indexes of the documents to pluck. Items are plucked in this order.


**`ignoreOutOfBounds`**  `boolean`

Ignore indexes that are out of bounds.


