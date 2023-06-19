# Mencari Data Attachment Berdasarkan ID Invoice
#### Endpoint
Penjelasan lebih lanjut bisa dilihat [disini](../list_api/search_data.md)

#### Parameter
| Key            | Type    | Description                                                                  |
| :---           | :---    | :---                                                                         |
| token          | string  | Isi dengan token                                                             |
| domain         | string  | [('res_model', '=', 'account.invoice'), ('res_id', '=', \<int:invoice_id\>)] |
| fields         | string  | ["name", "datas"]                                                            |

#### Contoh
```bash
import requests

params = {
    "login": "admin",
    "password": "admin"
}
response = requests.get("http://localhost:8069/api/user/get_token?", params=params)
json_data = response.json()
token = json_data["token"]

params = {
    "token": token,
    "domain": str([('res_model', '=', 'account.invoice'), ('res_id', '=', 12)]),
    "fields": str(["name", "datas"])
}

response = requests.get("http://localhost:8069/api/ir.attachment/search?", params=params)

print (response.content)
```
