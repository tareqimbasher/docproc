# <small>:nut_and_bolt:</small> Slice

Selects a range of documents and discards the rest.

### Accepts

  - `Any`

### Outputs

  - `Any`

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


