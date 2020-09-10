# Search Data
#### Endpoint
```
/api/<string:model>/search, /api/<string:model>/search/<int:id>
```

#### Parameters
| Parameter | Mandatory     | Description                          | Type               |
| :---      | :---          | :---                                 | :---               |
| token     | yes           | Token user                           | string             |
| domain    | no            | Kriteria pencarian data              | tuple dalam list   |
| offset    | no            | Banyaknya data yang akan diabaikan   | integer            |
| limit     | no            | Maksimal data yang akan dihasilkan   | integer            |

#### Output
- Tanpa Parameter

````bash
curl -i -d "token=858a5f372ea04cb7aad222fb6ba95f76" \
    https://demo8.simetri-sinergi.id/api/res.partner/search
`````
````json
[
    {"id": 3, "name": "Administrator"},
    {"id": 22, "name": "Bruce Banner"},
    {"id": 20, "name": "Clint Barton"},
    {"id": 12, "name": "Customer #1"},
    {...}
]
````

- Menggunakan parameter <b>id</b>

````bash
curl -i -d "token=858a5f372ea04cb7aad222fb6ba95f76" \
    https://demo8.simetri-sinergi.id/api/res.partner/search/22
````
````json
[{
    "name": "Bruce Banner",
    "company_id": [1, "Your Company"],
    "supplier": false,
    "customer": true,
    ...,
}]
````

- Menggunakan parameter <b>domain</b>
````bash
curl -i -d "token=858a5f372ea04cb7aad222fb6ba95f76&domain=[('ref', '=', 'ADM')]" \
    https://demo8.simetri-sinergi.id/api/res.partner/search
````
````json
[{"id": 22, "name": "Bruce Banner"}]
````
