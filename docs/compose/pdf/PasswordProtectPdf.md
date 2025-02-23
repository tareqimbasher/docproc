# <small>:nut_and_bolt:</small> PasswordProtect

Password-protects the contents of PDF documents.
   
### Formats

This action accepts and produces the following content type formats.

| Accepts | Produces |
|-----|-----|
|<ul><li>`application/pdf` _(.pdf)_</li></ul>|<ul><li>`application/pdf` _(.pdf)_</li></ul>|

### Usage

```js
{
  "kind": "PdfPasswordProtect",
  "ownerPassword": null,
  "userPassword": null
}
```
#### Properties

**`ownerPassword`**  `string` **Required**

The owner password.


**`userPassword`**  `string` **Required**

The user password.


