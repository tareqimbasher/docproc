# Get Merge Fields

`POST` **/v1/word/get-merge-field-names**

Accepts one word document and returns the names of all Mail Merge fields in the document.

## Usage

Use a `multipart/form-data` request body with one part:

**`file`** **(required)**

Add a `file` part for the Word document to upload. 
Be sure to add a valid `Content-Disposition` and `Content-Type` header.

#### Example

```js
POST /v1/word/get-merge-field-names
Content-Type: multipart/form-data; boundary=----BOUNDRYNAME

------BOUNDRYNAME
Content-Disposition: form-data; name="file"; filename="/path/to/document.docx"
Content-Type: application/vnd.openxmlformats-officedocument.wordprocessingml.document

(data)
------BOUNDRYNAME--
```

## Response

This response shows 2 merge fields, one named `Title` and the other `FirstName`.

```js
[
  "Title",
  "FirstName"
]
```