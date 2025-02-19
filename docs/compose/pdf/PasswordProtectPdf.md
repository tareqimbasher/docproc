# <small>:nut_and_bolt:</small> PasswordProtect

Password-protects the contents of PDF documents.

### Supported Inputs

  - `application/pdf`

### Possible Outputs

  - `application/pdf`

### JSON

```js
{
  "kind": "PdfPasswordProtect",
  "ownerPassword": null,
  "userPassword": null
}
```
### Properties

  - `ownerPassword` [`String`]: The owner password.
  - `userPassword` [`String`]: The user password.
