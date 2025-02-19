# <small>:nut_and_bolt:</small> Pluck

Selects any number of documents and discards the rest.

### Supported Inputs

  - `Any`

### Possible Outputs

  - `Any`

### JSON

```js
{
  "kind": "Pluck",
  "indexes": [],
  "ignoreOutOfBounds": false
}
```
### Properties

  - `indexes` [`Int32[]`] **Required**: 0-based indexes of the documents to pluck. Items are plucked in this order.
  - `ignoreOutOfBounds` [`Boolean`]: Ignore indexes that are out of bounds.
