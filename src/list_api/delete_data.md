# Delete Data
#### Endpoint
```
/api/<string:model>/unlink, /api/<string:model>/unlink/<int:id>
```
#### Parameters
| Parameter   | Mandatory     | Description                          | Type         |
| :---        | :---          | :---                                 | :---         |
| token       | yes           | Token user                           | string       |
| unlink_ids  | no            | List of ID yang akan dihaous         | list         |

#### Output
- Menggunakan parameter <b>id</b>
````bash
curl -i -d "token=858a5f372ea04cb7aad222fb6ba95f76" \
    https://demo8.simetri-sinergi.id/api/res.partner/unlink/28
`````
````json
{"success": "Records Successfully Deleted ID - 28"}
````

- Menggunakan parameter <b>unlink_ids</b>
````bash
curl -i -d "token=858a5f372ea04cb7aad222fb6ba95f76&unlink_ids=[22,23,24]" \
    https://demo8.simetri-sinergi.id/api/res.partner/unlink
`````
````json
{"success": "Records Successfully Deleted ID - [22,23,24]"}
````
