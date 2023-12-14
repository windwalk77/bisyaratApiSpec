# Sub Kategori API Spec


## Get All Sub Kategori

Penjelasan : Untuk mendapatkan semua sub kategori

Endpoint : GET /api/subkategori


Response Body Success :

```json
{
  "data": [
    {
    "id" : "1",
    "nama_kategori" : "Warna",
    "penjelasan" : "Pada bagian ini berisi warna ...."
  } , 
  {
    "id" : "2",
    "nama_kategori" : "Ekspresi",
    "penjelasan" : "Pada bagian ini berisi ekspresi ...."
  }
  ]
}
```

Response Body Error :

```json
{
  "errors": "Unauthorized"
}
```
