# Document Processor

An web service to process and transform documents.

## Build & Run

```shell
cd src/DocProcessor
dotnet watch run
```

You can then access the app at:

- **API**: https://localhost:7014/v1
- **Swagger**: https://localhost:7014/swagger/index.html

## Postman Collection

Import the `postman_collection.json` file in Postman to test.
The Swagger UI doesn't do well with multiform data and will fail on some endpoints. 