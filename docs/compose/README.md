# Compose API

`POST` **/v1/compose**

The endpoint accepts one or more documents, and a collection of [`Actions`](#actions) to run on those documents.

## Usage


Use a `multipart/form-data` request body with the following parts:

**`file`** **(required)**

Add one more `file` parts for each document to upload. 
Be sure to add valid `Content-Disposition` and `Content-Type` headers for each.

**`request`** **(required)**

Add one `request` part that contains a JSON string with the [`compose request`](#request).


#### Example

This request would split a PDF document into multiple documents, one per page. 

```js
POST /v1/compose
Content-Type: multipart/form-data; boundary=----BOUNDRYNAME

------BOUNDRYNAME
Content-Disposition: form-data; name="file"; filename="/path/to/document.pdf"
Content-Type: application/pdf

(data)
------BOUNDRYNAME
Content-Disposition: form-data; name="request"

{
  "actions": [
    [
      {"kind": "PdfSplit"}
    ]
  ]
}
------BOUNDRYNAME--
```

#### Request

The `request` part should be a JSON serialized string of the following object:

```js
{
  "actions": [...],
  "refFiles": [...]
}
```

##### Properties

**`actions`** `Action[]` **Required**

An array of actions to run.

**`refFiles`** `int[]`

If specified, defines which files that were uploaded should be considered reference documents that are referenceed and used in actions, but not documents that should be operated on themselves.

#### Response

The endpoint will respode with `200 OK` and a stream with the output document.

The response will also contain a `Content-Type` header with the mimetype of the output document. If the action workflow resulted in multiple documents, the response will be a `.zip` file containing all output documents with the `Content-Type` set to `application/zip`.

## Actions

An action is a way to express a transformation to the compose pipeline.

- Each action has a `kind` property reflecting its type.
- An action may have one or more other properties (options) that are specific to that action.
- Actions are ran sequentially.
- When an action runs, it takes the output from the previous step as input. It then applies its transformation to the document(s) and the output is then used for the next action.
- The format (content type) an action accepts as input varies from one action to another. The format an action produces as output also varies just the same.

> Actions are documented in groups under the `Compose` sidebar item.

#### Example

```js
{
  "actions": [
    {
      "kind": "WordMailMerge",
      "data": {
        "FirstName": "John",
        "LastName": "Doe"
      }
    },
    {
      "kind": "WordConvertToPdf"
    },
    {
      "kind": "PdfCompress"
    }
  ]
}
```

This request contains 3 actions:

1. First the Word document is mail merged using the provided data. `kind` = [`WordMailMerge`](/compose/word/MailMergeWordAction.md)
2. The next action converts the Word document to a PDF. `kind` = [`WordConvertToPdf`](/compose/word/ConvertToPdfWordAction.md)
3. Finally, the PDF is compressed to reduce its size. `kind`= [`PdfCompress`](/compose/pdf/CompressPdfAction.md)


#### Common Properties

These properties are common to all actions.

```js
{
    "kind": "...",
    "continueOnError": false
}
```

**`kind`** `ActionKind` **Required**

A discriminator that identifies the type of action.

**`continueOnError`** `boolean`

If true and an error occurs while running an action, the error is ignored and processing resumes with the next action.