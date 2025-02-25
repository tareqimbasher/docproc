# Get Structure

`POST` **/v1/word/get-structure**

Accepts one word document and returns a JSON structure representing the structure, or DOM (Document Object Model), of the document. This information can then be used to run [Word Edit Actions](/compose/word/EditWordAction.md) on that document using the [`Compose API`](/compose/).

## Usage

Use a `multipart/form-data` request body with one part:

**`file`** **(required)**

Add a `file` part for the Word document to upload. 
Be sure to add a valid `Content-Disposition` and `Content-Type` header.

#### Example

```js
POST /v1/word/get-structure
Content-Type: multipart/form-data; boundary=----BOUNDRYNAME

------BOUNDRYNAME
Content-Disposition: form-data; name="file"; filename="/path/to/document.docx"
Content-Type: application/vnd.openxmlformats-officedocument.wordprocessingml.document

(data)
------BOUNDRYNAME--
```

## Response

This a sample response structure of a document with 2 paragraphs, the first containing some text and the second containing an image (picture).

```js
{
  "title": "",
  "subject": "",
  "author": "John Doe",
  "lastAuthor": "John Doe",
  "company": "",
  "template": "Normal.dotm",
  "protectionType": "NoProtection",
  "pageCount": 1,
  "wordCount": 5,
  "revisionNumber": "16",
  "createDate": "2025-01-19T14:53:00Z",
  "lastSaveDate": "2025-01-20T00:47:00Z",
  "lastPrintDate": "0001-01-01T00:00:00",
  "sections": [
    {
      "textBody": {
        "path": "/sections/0[Section]/items/0[TextBody]",
        "items": [
          {
            "kind": "Paragraph",
            "path": "/sections/0[Section]/items/0[TextBody]/items/0[Paragraph]",
            "items": [
              {
                "kind": "TextRange",
                "path": "/sections/0[Section]/items/0[TextBody]/items/0[Paragraph]/items/0[TextRange]",
                "text": "This is some sample text"
              }
            ]
          },
          {
            "kind": "Paragraph",
            "path": "/sections/0[Section]/items/0[TextBody]/items/1[Paragraph]",
            "items": [
              {
                "kind": "Picture",
                "path": "/sections/0[Section]/items/0[TextBody]/items/1[Paragraph]/items/0[Picture]",
                "name": "Picture 1",
                "title": null,
                "altText": null,
                "width": 128,
                "height": 128,
                "size": 13450,
                "fileRef": null
              }
            ]
          }
        ]
      }
    }
  ]
}
```