# Kategori API Spec

## Get All Kategori

Penjelasan : Untuk mendapatkan semua kategori 

Endpoint : GET /api/kategori


Response Body Success :

```json
{
  "data": [
    {
    "id" : "1",
    "nama_kategori" : "Kata",
    "penjelasan" : "Pada bagian ini berisi kata ...."
  } , 
  {
    "id" : "2",
    "nama_kategori" : "Kalimat",
    "penjelasan" : "Pada bagian ini berisi kalimat ...."
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

