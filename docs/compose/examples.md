# Examples

### Example 1

A word document is mail merged, then converted to a PDF, then compressed to reduce its size and finally returned.

```mermaid
flowchart LR
    0(Client)
    0 -->|.docx| A[WordMailMerge]
    A -->|.docx| B[WordConvertToPdf] --> |.pdf| C[PdfCompress]
    C -->|.pdf| E(Return)
    E -->|.pdf| 0
```

#### Request

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

### Example 2

A word document is mail merged, then converted to a PDF, then split into multiple documents which are individually compressed. They are then returned to the client as a zip file.

```mermaid
flowchart LR
    0(Client)
    0 -->|.docx| A[WordMailMerge]
    A -->|.docx| B[WordConvertToPdf] --> |.pdf| C[PdfSplit]
    C -->|.pdf| E[PdfCompress] 
    C -->|.pdf| E
    E -->|.pdf| F(Return)
    E -->|.pdf| F
    F -->|.zip| 0
```

#### Request

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
    { "kind": "PdfSplit" },
    { "kind": "PdfCompress" }
  ]
}
```

### Example 3

**Use case:** We have 2 documents. We want to create one new document that contains the first page of each of the 2 input documents.

2 PDF documents are passed, the first has 2 pages and the second has 3 pages. Each is split, resulting in 5 separate PDF documents. Then we use [`Pluck`](/compose/common/PluckAction.md) to select the items we want to keep: index 0 and 2 (the first page of each of the original documents). Finally, we merge the 2 documents into a new PDF and return.

```mermaid
flowchart LR
    0(Client)
    0 -->|.pdf - 2 pages| A[PdfSplit]
    0 -->|.pdf - 3 pages| A
    A -->|.pdf| B[Pluck 0,2]
    A -->|.pdf| B
    A -->|.pdf| B
    A -->|.pdf| B
    A -->|.pdf| B
    B --> |.pdf| C[PdfMerge]
    B --> |.pdf| C
    C -->|.pdf| D(Return)
    D -->|.pdf| 0
```

#### Request

```js
{
  "actions": [
    { "kind": "PdfSplit" },
    {
        "kind": "Pluck",
        "indexes": [0, 2]
    },
    { "kind": "PdfMerge" }
  ]
}
```