# Compose API

`POST` **/v1/compose**

This endpoint processes one or more documents (files) using a series of [`Actions`](#actions) specified in the request.

## Usage


Construct  a `multipart/form-data` request body containing the following parts:

**`file`** **(Required)**

- Include one or more file parts—one for each document to be uploaded.
- Ensure that each file part includes valid Content-Disposition and Content-Type headers.

**`request`** **(Required)**

- Include a single `request` part that contains a JSON-serialized [`ComposeRequest`](#ComposeRequest) object. This object defines the actions to be applied to the uploaded documents.

#### Example

Below is an example of a multipart/form-data request body:

- **Part 1** (`file`): Contains the document to be uploaded (e.g., `document.pdf`).
- **Part 2** (`request`): Contains a JSON object (a [`ComposeRequest`](#ComposeRequest)) with an action to split the PDF into multiple documents, one per page.

When the request is processed, the API will apply the specified actions to the uploaded files and return the resulting documents.

```js
POST /v1/compose
Content-Type: multipart/form-data; boundary=----BOUNDRY7MA4YWxkTrZu0gW

------BOUNDRY7MA4YWxkTrZu0gW
Content-Disposition: form-data; name="file"; filename="/path/to/document.pdf"
Content-Type: application/pdf

(data)
------BOUNDRY7MA4YWxkTrZu0gW
Content-Disposition: form-data; name="request"

{
  "actions": [
    [
      {"kind": "PdfSplit"}
    ]
  ]
}
------BOUNDRY7MA4YWxkTrZu0gW--
```

> See the [Examples](/compose/examples.md) page for more.

#### ComposeRequest

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

_(Optional)_ An array of indexes identifying which uploaded files should be treated as reference documents. Files listed in this array are not processed by the actions — they serve solely as external references for actions that support including reference documents.

#### Response

The endpoint returns a `200 OK` status along with a stream containing the output document. The response's `Content-Type` header will indicate the [MIME type](https://developer.mozilla.org/en-US/docs/Web/HTTP/MIME_types) of the output document.

If the applied actions produce multiple documents, the response will be a `.zip` archive containing all output files, and the `Content-Type` will be set to `application/zip`.

## Actions

An action represents a transformation step within the compose pipeline.

- Each action includes a `kind` property that identifies its type.
- Some actions have additional properties (options).
- Actions are executed sequentially.
- Each action processes the output from the previous step, applies its transformation, and passes its output to the next action.
- The input and output formats (content types) of an action may vary depending on its functionality.

> Detailed documentation for each action is available under the `Compose` sidebar item.

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
    { "kind": "WordConvertToPdf" },
    { "kind": "PdfCompress" }
  ]
}
```

This request contains 3 actions:

1. First the Word document is mail merged using the data mapping. `kind` = [`WordMailMerge`](/compose/word/MailMergeWordAction.md)
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