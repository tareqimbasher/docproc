# <small>:nut_and_bolt:</small> Scale

Scales (resizes) an image to new dimensions.

### Accepts

  - `image/png` _(.png)_
  - `image/jpeg` _(.jpg)_
  - `image/webp` _(.webp)_
  - `image/bmp` _(.bmp)_
  - `image/heif` _(.heif)_

### Produces

  - `image/png` _(.png)_

### Usage

```js
{
  "kind": "ImageScale",
  "width": null,
  "height": null,
  "quality": 100
}
```
#### Properties

**`width`**  `int32?`

If specified, the image will be scaled to this width. Otherwise the original width is used. Cannot be null if Height is null.


**`height`**  `int32?`

If specified, the image will be scaled to this height. Otherwise the original height is used. Cannot be null if Width is null.


**`quality`**  `int32`

A value between 1 and 100 indicating the quality of the scaled image.


