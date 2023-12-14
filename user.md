# User API Spec

## Register User

Penjelasan : Untuk register user

Endpoint : POST /api/users

Request Body :

```json
{
  "email": "test@gmail.com",
  "username": "test",
  "password": "pass",
  "name": "ini tes"
}
```

Response Body Success :

```json
{
  "data": {
    "id" : "1",
    "email": "test@gmail.com",
    "username": "test",
    "name": "ini tes"
  }
}
```

Response Body Error :

```json
{
  "errors": "Email is already used , dll"
}
```

## Login User

Penjelasan : Untuk login user

Endpoint : POST /api/users/login

Request Body :

```json
{
  "email": "test@gmail.com",
  "password": "pass"
}
```

Response Body Success :

```json
{
  "data": {
    "token": "unique-token"
  }
}
```

Response Body Error :

```json
{
  "errors": "Email or Password is wrong"
}
```

## Update User

Penjelasan : Untuk update data user yang login sekarang

Endpoint : PATCH /api/users/current

Headers :

- Authorization : token

Request Body :

```json
{
  "email": "test@gmail.com", //optional
  "username": "test", // optional
  "password": "pass", // optional
  "name": "ini tes" // optional
}
```

Response Body Success :

```json
{
  "data": {
    "id" : "1",
    "email": "test@gmail.com",
    "username": "test",
    "name": "ini tes"
  }
}
```

Response Body Error :

```json
{
  "errors": "Email is already used , dll"
}
```

## Get Current User

Penjelasan : Untuk mendapatkan data user yang login sekarang

Endpoint : GET /api/users/current

Headers :

- Authorization : token

Response Body Success :

```json
{
  "data": {
    "id" : "1",
    "email": "test@gmail.com",
    "username": "test",
    "name": "ini tes"
  }
}
```

Response Body Error :

```json
{
  "errors": "Unauthorized"
}
```

## Logout User

Penjelasan : Untuk logout user

Endpoint : DELETE /api/users/logout

Headers :

- Authorization : token

Response Body Success :

```json
{
  "data": "Logout success"
}
```

Response Body Error :

```json
{
  "errors": "Unauthorized"
}
```
