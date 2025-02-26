# <small>:nut_and_bolt:</small> Convert

Converts images to other formats.
   
### Formats

This action can accept and produce the following content type formats.

| Accepts | Produces |
|-----|-----|
|<ul><li>`image/png` _(.png)_</li><li>`image/jpeg` _(.jpg)_</li><li>`image/webp` _(.webp)_</li></ul>|<ul><li>`image/png` _(.png)_</li><li>`image/jpeg` _(.jpg)_</li><li>`image/webp` _(.webp)_</li></ul>|

### Usage

```js
{
  "kind": "ImageConvert",
  "format": "PNG",
  "quality": 100
}
```
### Properties

**`format`**  [`ImageConvertFormat`](#ImageConvertFormat) **Required**

The format to convert to.


**`quality`**  `int32`

A value between 1 and 100 indicating the quality of the converted image. Default is **100**.


### Relevant Types

#### ImageConvertFormat

Image formats that can be used for conversions.

```js
PNG
JPEG
WEBP
```
---
