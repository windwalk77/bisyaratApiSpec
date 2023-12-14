# Feedback API Spec

## Create Feedback

Penjelasan : Untuk membuat Feedback

Endpoint : POST /api/feedback

Headers :

- Authorization : token

Request Body :

```json
{
  "keterangan": "Aplikasi ini membutuhkan ..."
}
```

Response Body Success :

```json
{
  "data": {
    "id": "1",
    "keterangan": "Aplikasi ini membutuhkan ...",
    "username": "test"
  }
}
```

Response Body Error :

```json
{
  "errors": "Unauthorized"
}
```
