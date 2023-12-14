# Kata API Spec


## Get Kata by ID

Penjelasan : Untuk mendapatkan kata berdasarkan ID kata nya

Endpoint : GET /api/kata/:id

Response Body Success :

```json
{
  "data": {
    "id": "1",
    "kata": "Satu",
    "url_video": "www.satu.mp4",
    "penjelasan": "Ini adalah bahasa isyarat untuk angka satu",
    "nama_kategori": "Angka",
    "nama_sub_kategori": "Angka"
  }
}
```

Response Body Error :

```json
{
  "errors": "Id is wrong"
}
```

## Get Kata and status 
Penjelasan : Untuk mendapatkan kata dan status nya berdasarkan query params

Endpoint : GET /api/kata/status

Headers :
- Authorization : token

Query Params (Hanya gunakan salah satu) : 
- nama_kategori : nama dari kategori,
- nama_sub_kategori : nama dari sub kategori

Response Body Success :

```json
{
  "data": {
    "id": 1,
    "kata": "Satu",
    "riwayat_belajar": [
      {
        "status": false
      }
    ]
  }
}
```

Response Body Error :

```json
{
  "errors": "Kategori is wrong"
}
```


