# <small>:nut_and_bolt:</small> Scale

Scales (resizes) an image to new dimensions.

### Accepts

  - `image/png`
  - `image/x-png`
  - `image/jpeg`
  - `image/webp`
  - `image/bmp`
  - `image/heif`

### Outputs

  - `image/png`
  - `image/x-png`
  - `image/jpeg`
  - `image/webp`
  - `image/bmp`
  - `image/heif`

### Usage

```js
{
  "kind": "ImageScale",
  "width": null,
  "height": null
}
```
#### Properties

**`width`**  `int32?`

If specified, the image will be scaled to this width. Otherwise the original width is used. Cannot be null if Height is null.


**`height`**  `int32?`

If specified, the image will be scaled to this height. Otherwise the original height is used. Cannot be null if Width is null.


