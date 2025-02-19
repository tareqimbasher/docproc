# Scale

Scales (resizes) an image to new dimensions.

### Supported Inputs

  - `image/png`
  - `image/x-png`
  - `image/jpeg`
  - `image/webp`
  - `image/bmp`
  - `image/vnd.wap.wbmp`
  - `image/heif`

### Possible Outputs

  - `image/png`
  - `image/x-png`
  - `image/jpeg`
  - `image/webp`
  - `image/bmp`
  - `image/vnd.wap.wbmp`
  - `image/heif`

### JSON

```js
{
  "kind": "ImageScale",
  "width": null,
  "height": null
}
```
### Properties

  - `width` [`Int32?`]: If specified, the image will be scaled to this width. Otherwise the original width is used. Cannot be null if Height is null.
  - `height` [`Int32?`]: If specified, the image will be scaled to this height. Otherwise the original height is used. Cannot be null if Width is null.
