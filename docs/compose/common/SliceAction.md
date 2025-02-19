# <small>:nut_and_bolt:</small> Slice

Selects a range of documents and discards the rest.

### Supported Inputs

  - `Any`

### Possible Outputs

  - `Any`

### JSON

```js
{
  "kind": "Slice",
  "skip": null,
  "take": null,
  "reverse": false
}
```
### Properties

  - `skip` [`Int32?`]: How many items to skip.
  - `take` [`Int32?`]: How many items to take.
  - `reverse` [`Boolean`]: Whether to skip/take starting from the end; ie. `Skip = 1` in this case will skip the last document.
