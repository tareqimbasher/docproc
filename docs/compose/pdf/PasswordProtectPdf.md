# <small>:nut_and_bolt:</small> PasswordProtect

Password-protects the contents of PDF documents.

### Accepts

  - `application/pdf` _(.pdf)_

### Produces

  - `application/pdf` _(.pdf)_

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


